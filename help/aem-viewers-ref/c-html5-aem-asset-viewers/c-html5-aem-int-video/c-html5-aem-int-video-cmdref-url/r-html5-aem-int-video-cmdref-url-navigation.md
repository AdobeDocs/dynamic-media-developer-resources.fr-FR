---
description: URL de la visionneuse de vidéos interactive.
solution: Experience Manager
title: navigation
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 12%

---

# navigation{#navigation}

URL de la visionneuse de vidéos interactive.

` navigation= *`file`*`

Le lecteur prend en charge la navigation dans les chapitres vidéo au moyen de fichiers WebVTT hébergés. Les opérateurs de positionnement des indices ne sont pas pris en charge.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier</span> </span> </p> </td> 
   <td colname="col2"> <p> Indique une URL ou un chemin d’accès au contenu de navigation WebVTT. Image Serving doit héberger le fichier WebVTT. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```
