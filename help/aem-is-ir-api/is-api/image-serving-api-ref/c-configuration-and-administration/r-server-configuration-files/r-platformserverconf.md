---
description: Contient [!DNL Platform Server] des paramètres.
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# PlatformServer.conf{#platformserver-conf}

Contient [!DNL Platform Server] des paramètres.

Ce fichier est un fichier de propriétés JAVA. Il faut veiller à suivre les conventions appropriées ; sinon, le [!DNL Platform Server] risque de ne pas démarrer. Utilisez une double barre oblique inverse « \\ » ou une barre oblique simple « / » au lieu d’une barre oblique inverse « \ » dans les chemins d’accès aux fichiers Windows. La barre oblique inverse est utilisée comme caractère d’échappement dans ce type de fichier.

Les modifications apportées à ce fichier prennent effet après l’enregistrement du fichier.

Seuls les paramètres répertoriés ci-dessous peuvent être modifiés dans [!DNL PlatformServer.conf]. Si un paramètre particulier est absent, il peut être ajouté n’importe où dans le fichier. Seule une occurrence de chaque paramètre peut être présente.

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Paramètres généraux [!DNL Platform Server] </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=./cache </span> </p> <p> <span class="codeph"> cache.maxEntries=1000000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=.contenu statique </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuration de la grappe de cache </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span>&lt;/empty&gt; </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Erreur de configuration de redirection </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span>&lt;/empty&gt; </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Configuration SVG </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> svgProvider.rootPaths=./Images </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> svgProvider.port=8080 </span> </p> <p> <span class="codeph"> svgProvider.fontRoot=./Images </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Réponses de la visionneuse de médias </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.nestingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>
