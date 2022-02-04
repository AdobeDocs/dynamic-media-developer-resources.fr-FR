---
title: VideoPlayer.singleclick
description: Attribut de configuration pour la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attribut de configuration pour la visionneuse de vidéos.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage d’un clic/d’un clic pour activer/désactiver la lecture/la pause. Définir sur <span class="codeph"> none</span> désactive la fonction cliquer/appuyer une seule fois pour lire/mettre en pause. Si la variable est définie sur <span class="codeph"> playPause</span>, un clic sur la vidéo fait basculer entre la lecture et la mise en pause de la vidéo. Sur certains périphériques, vous pouvez utiliser des contrôles natifs. Dans ce cas, <span class="codeph"> singleclick</span> Le comportement est désactivé. </p> </td> 
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
