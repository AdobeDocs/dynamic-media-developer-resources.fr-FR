---
title: SmartCropVideoPlayer.initialbitrate
description: Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4fc4fefa-b094-4e2e-b8ec-a439f8a1a56c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

Attribut de configuration pour la visionneuse de vidéos.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Définit le débit vidéo (en kilobits par seconde ou en kbit/s) utilisé pour la lecture initiale de la vidéo sur les ordinateurs de bureau. </p> <p>Si cette valeur de débit n’existe pas dans la visionneuse de vidéos adaptative, le lecteur vidéo démarre la vidéo dont le débit est le plus faible suivant. </p> <p>Si la variable est définie sur <span class="codeph"> 0 </span>, le lecteur vidéo démarre à partir du débit le plus bas possible. Applicable uniquement aux systèmes qui ne prennent pas en charge la vidéo HLS HTML5 (navigateurs Firefox, Chrome et Internet Explorer 11 sous Windows 10) et lorsque le mode de lecture est défini sur <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
