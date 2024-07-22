---
title: interactivedata
description: Commande URL de la visionneuse de vidéos interactives.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 4%

---

# interactivedata{#interactivedata}

Commande URL de la visionneuse de vidéos interactives.

`interactivedata= *`file`*`

Les données interactives associent certaines régions temporelles du contenu vidéo aux données de produit qui s’affichent ultérieurement dans des échantillons interactifs en regard de la vidéo. Elle est également associée au panneau d’appel à l’action affiché à la fin de la lecture vidéo. Il fournit également un titre pour la vidéo interactive affichée dans le panneau d’appel à l’action.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fichier</span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie une URL ou un chemin d’accès au contenu de données interactives WebVTT. Le fichier WebVTT doit être traité par le serveur d’images. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

Aucune

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
