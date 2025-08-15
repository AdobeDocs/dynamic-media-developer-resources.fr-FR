---
title: VideoPlayer.singleclick
description: Attribut de configuration pour la visionneuse vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attribut de configuration pour la visionneuse vidéo.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`aucun|playPause`*`

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
