---
description: L’utilitaire playlog permet de prégénérer le contenu du cache de réponse HTTP.
solution: Experience Manager
title: Utilitaire "playlog"
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---


# Utilitaire &#39;playlog&#39;{#the-playlog-utility}

L’utilitaire playlog permet de prégénérer le contenu du cache de réponse HTTP.

Le cache de réponse HTTP Image Serving existant n’est pas garanti utilisable après une mise à niveau de version majeure (lorsque le premier ou le deuxième chiffre du numéro de version a changé). Si le serveur doit être mis en service après la mise à niveau, le serveur peut être surchargé en raison des premières heures de demandes de mise en cache manquées jusqu’à ce que le cache soit raisonnablement rempli et que le taux d’accès du cache augmente.

Pour éviter ce pic de chargement initial, l&#39;utilitaire `playlog` peut être utilisé pour prégénérer le contenu du cache de réponse HTTP. `playlog` extrait les requêtes HTTP d’un fichier journal d’accès existant et les envoie au serveur pour générer des entrées de cache. Pour les scénarios d’utilisation types, il suffit de lire un seul fichier journal d’accès contenant l’équivalent d’une journée de trafic.

Outre l’amorçage du cache de réponse HTTP après l’installation de la mise à niveau, l’utilitaire est également utilisé pour prégénérer le contenu du cache lors de l’ajout d’un nouveau serveur à un environnement à charge équilibrée ; il suffit de lire un fichier journal récent d&#39;un des autres serveurs.

`playlog` peut être configuré pour prendre en charge la plupart des fichiers journaux d’accès générés par des versions antérieures d’Image Serving.

## Utilisation {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> préfixe  </span> </span> </p> </td> 
  <td class="stentry"> <p>URL racine pour ajouter en préfixe les requêtes extraites du fichier journal. </p> <p>Par défaut : <span class="filepath"> http://localhost:8080/is </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro de champ (colonne) contenant la demande dans l'enregistrement du journal ; basé sur 1. </p> <p>Par défaut : 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> séparateur  </span> </span> </p> </td> 
  <td class="stentry"> <p>Séparateur de champ ; modèle d’expression régulier. </p> <p>Par défaut: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> marqueur  </span> </span> </p> </td> 
  <td class="stentry"> <p>Marqueur de demande ; identifie les requêtes du fichier journal qui doivent être lues ; modèle d’expression régulier. </p> <p>Par défaut : Demande <span class="codeph"> : </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> suffixe  </span> </span> </p> </td> 
  <td class="stentry"> <p>Suffixe à ajouter à la requête extraite du fichier journal ; peut être utilisé pour séparer les requêtes lues des requêtes actives dans les fichiers journaux ; a '?' ou le séparateur "&amp;" est inséré automatiquement ; peut référencer n’importe quel champ de journal par position dans les accolades, la valeur par défaut correspond au champ de signature md5. </p> <p>Par défaut : <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>En mode détaillé, imprime les URL de requête générées dans <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Imprimez un synopsis dans <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - méthode de requête HTTP à utiliser ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Par défaut : <span class="codeph"> smart </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos dans le fichier journal pour saisir la méthode d'origine. </p> <p>Par défaut : 15 </p> </td> 
 </tr> 
</table>

Sous Windows, le nom de fichier est [!DNL playlog.bat] et sous Linux, il est [!DNL playlog.sh].

## Exemples {#section-716e5c35e9fa4ee3a4b0687381fcea40}

L’exemple suivant lit toutes les requêtes d’un fichier journal d’accès créé par Image Serving sous Linux :

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

La commande suivante lit toutes les requêtes trouvées dans un fichier journal de suivi créé par Image Serving sous Windows :

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
