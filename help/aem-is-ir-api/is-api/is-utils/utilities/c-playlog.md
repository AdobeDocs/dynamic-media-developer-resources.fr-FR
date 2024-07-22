---
description: L’utilitaire playlog peut être utilisé pour prégénérer le contenu pour le cache de réponse HTTP.
solution: Experience Manager
title: Utilitaire 'playlog'
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Utilitaire &#39;playlog&#39;{#the-playlog-utility}

L’utilitaire playlog peut être utilisé pour prégénérer le contenu pour le cache de réponse HTTP.

Le cache de réponse HTTP du serveur d’images existant n’est pas garanti utilisable après une mise à niveau de version majeure (lorsque le premier ou le deuxième chiffre du numéro de version a changé). Si le serveur doit être mis en service après la mise à niveau, il peut être surchargé en raison des premières heures de requêtes de mise en cache manquées, jusqu’à ce que le cache soit raisonnablement rempli et que le taux d’accès au cache augmente.

Pour éviter ce pic de chargement initial, l’utilitaire `playlog` peut être utilisé pour prégénérer le contenu du cache de réponse HTTP. `playlog` extrait les requêtes HTTP d’un fichier journal d’accès existant et l’envoie au serveur pour générer les entrées de cache. Pour les scénarios d’utilisation standard, il suffit de lire un seul fichier journal d’accès contenant l’équivalent d’une journée de trafic.

En plus d’amorcer le cache de réponse HTTP après l’installation de la mise à niveau, l’utilitaire est également utilisé pour pré-générer le contenu du cache lors de l’ajout d’un nouveau serveur à un environnement à charge équilibrée. Il suffit de lire un fichier journal récent à partir de l’un des autres serveurs.

`playlog` peut être configuré pour prendre en charge la plupart des fichiers journaux d’accès générés par des versions antérieures du serveur d’images.

## Utilisation {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> préfixe </span> </span> </p> </td> 
  <td class="stentry"> <p>URL racine pour ajouter les requêtes extraites du fichier journal en préfixe. </p> <p>Par défaut : <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> col </span> </span> </p> </td> 
  <td class="stentry"> <p>Numéro du champ (colonne) qui contient la requête dans l’enregistrement de journal ; basé sur 1. </p> <p>Valeur par défaut : 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> separator </span> </span> </p> </td> 
  <td class="stentry"> <p>Séparateur de champ ; modèle d’expression régulière. </p> <p>Par défaut : <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> marqueur </span> </span> </p> </td> 
  <td class="stentry"> <p>Marqueur de requête ; identifie les requêtes du fichier journal qui doivent être lues ; modèle d’expression régulière. </p> <p>Valeur par défaut : <span class="codeph"> Request : </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> suffixe </span> </span> </p> </td> 
  <td class="stentry"> <p>Suffixe pour ajouter à la requête extraite du fichier journal ; peut être utilisé pour séparer les requêtes de lecture des requêtes en direct dans les fichiers journaux ; un "?" ou le séparateur "&amp;" est inséré automatiquement ; le suffixe peut référencer n’importe quel champ de journal par position entre accolades, la valeur par défaut correspond au champ de signature md5. </p> <p>Par défaut : <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>En mode verbeux, imprime les URL de requête générées sur <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>Imprimez une synthèse sur <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method - méthode de requête HTTP à utiliser ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Par défaut : <span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos dans le fichier journal pour obtenir la méthode d’origine. </p> <p>Valeur par défaut : 15 </p> </td> 
 </tr> 
</table>

Pour Windows, le nom de fichier est [!DNL playlog.bat] et sous Linux, il est [!DNL playlog.sh].

## Exemples {#section-716e5c35e9fa4ee3a4b0687381fcea40}

L’exemple suivant permet de lire toutes les requêtes d’un fichier journal d’accès créé par Image Serving sous Linux :

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

La commande suivante permet de lire toutes les requêtes trouvées dans un fichier journal de trace créé par Image Serving sous Windows :

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
