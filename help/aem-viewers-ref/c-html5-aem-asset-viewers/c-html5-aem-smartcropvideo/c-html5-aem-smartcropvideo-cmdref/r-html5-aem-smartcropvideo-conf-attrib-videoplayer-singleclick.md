---
title: SmartCropVideoPlayer.singleclick
description: Attribut de configuration pour la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 4%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Attribut de configuration pour la visionneuse de vidéos avec recadrage intelligent.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`aucun|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> aucun|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage d’un simple clic/appuyer pour basculer lecture/pause. La définition sur <span class="codeph"> aucun</span> désactive la lecture/mise en pause d’un simple clic/appuyer pour jouer. Si vous êtes configuré sur <span class="codeph"> lecturePause</span>, cliquez sur la vidéo pour basculer entre la lecture et la suspension de la vidéo. Sur certains appareils, vous pouvez utiliser des contrôles natifs. Dans ce cas, <span class="codeph"> le comportement d’un seul clic</span> est désactivé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```
