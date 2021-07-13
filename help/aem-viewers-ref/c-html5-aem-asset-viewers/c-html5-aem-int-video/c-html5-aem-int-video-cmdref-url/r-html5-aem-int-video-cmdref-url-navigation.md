---
description: Commande URL de la visionneuse de vidéos interactives.
solution: Experience Manager
title: navigation
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 12%

---

# navigation{#navigation}

Commande URL de la visionneuse de vidéos interactives.

` navigation= *`file`*`

La visionneuse prend en charge la navigation par chapitre vidéo au moyen de fichiers WebVTT hébergés. Les opérateurs de positionnement des repères ne sont pas pris en charge.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier</span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie une URL ou un chemin d’accès au contenu de navigation WebVTT. Le serveur d’images doit héberger le fichier WebVTT. </p> </td> 
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
