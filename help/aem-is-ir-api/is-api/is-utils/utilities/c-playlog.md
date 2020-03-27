---
description: L’utilitaire playlog peut être utilisé pour prégénérer le contenu du cache de réponse HTTP.
seo-description: L’utilitaire playlog peut être utilisé pour prégénérer le contenu du cache de réponse HTTP.
seo-title: Utilitaire "playlog"
solution: Experience Manager
title: Utilitaire "playlog"
topic: Scene7 Image Serving - Image Rendering API
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Utilitaire &quot;playlog&quot;{#the-playlog-utility}

L’utilitaire playlog peut être utilisé pour prégénérer le contenu du cache de réponse HTTP.

Le cache de réponse HTTP de diffusion d’images n’est pas garanti utilisable après une mise à niveau majeure de la version (lorsque le premier ou le deuxième chiffre du numéro de version a changé). Si le serveur doit être mis en service après la mise à niveau, le serveur peut être surchargé en gérant les premières heures de demandes d’abandon du cache jusqu’à ce que le cache soit raisonnablement rempli et que le taux d’accès au cache augmente.

Pour éviter ce pic de chargement initial, l’ `playlog` utilitaire peut être utilisé pour prégénérer le contenu du cache de réponse HTTP. `playlog` extrait les requêtes HTTP d’un fichier journal d’accès existant et les envoie au serveur pour générer des entrées de cache. Pour les scénarios d’utilisation standard, il suffit de lire un fichier journal d’accès unique contenant une journée entière de trafic.

En plus d&#39;amorcer le cache de réponse HTTP après l&#39;installation de la mise à niveau, l&#39;utilitaire est également utilisé pour prégénérer le contenu du cache lors de l&#39;ajout d&#39;un nouveau serveur à un  de  avec équilibrage de charge; il suffit de lire un fichier journal récent d&#39;un des autres serveurs.

`playlog` peut être configuré pour prendre en charge la plupart des fichiers journaux d’accès générés par des versions antérieures de la diffusion d’images.

## Utilisation {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> préfixe </span></span> </p> </td> 
  <td class="stentry"> <p>URL racine pour ajouter en préfixe les requêtes extraites du fichier journal. </p> <p>Valeur par défaut : <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span></span> </p> </td> 
  <td class="stentry"> <p>numéro de champ (colonne) contenant la requête dans l'enregistrement du journal; 1. </p> <p>Valeur par défaut : 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> séparateur </span></span> </p> </td> 
  <td class="stentry"> <p>Séparateur de champ; modèle  régulier . </p> <p>Par défaut: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> marqueur </span></span> </p> </td> 
  <td class="stentry"> <p>Marqueur de requête ; identifie les requêtes du fichier journal qui doivent être lues ; modèle  régulier . </p> <p>Valeur par défaut : <span class="codeph"> Requête : </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> suffixe </span></span> </p> </td> 
  <td class="stentry"> <p>Suffixe à ajouter à la requête extraite du fichier journal ; peut être utilisé pour séparer les requêtes en lecture différée des requêtes actives dans les fichiers journaux ; a '?' ou le séparateur "&amp;" est inséré automatiquement ; peut faire référence à n’importe quel champ de journal par position dans les accolades, la valeur par défaut correspond au champ de signature md5. </p> <p>Valeur par défaut : <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>En mode détaillé, imprime les URL de requête générées vers <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>Imprimez un synopsis dans <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - méthode de requête HTTP à utiliser ( <span class="codeph"> |get|post|head|smart </span>). </p> <p>Valeur par défaut : <span class="codeph"> intelligent </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos dans le fichier journal à partir duquel récupérer la méthode d’origine. </p> <p>Valeur par défaut : 15 </p> </td> 
 </tr> 
</table>

Sous Windows, le nom du fichier est [!DNL playlog.bat] et sous Linux, il est [!DNL playlog.sh].

## Exemples {#section-716e5c35e9fa4ee3a4b0687381fcea40}

L’exemple suivant lit toutes les requêtes d’un fichier journal d’accès créé par Image Serving sous Linux :

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

La commande suivante lit toutes les requêtes trouvées dans un fichier journal de suivi créé par Image Serving sous Windows :

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
