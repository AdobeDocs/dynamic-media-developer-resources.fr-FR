---
description: Attribut de configuration pour la visionneuse vidéo.
seo-description: Attribut de configuration pour la visionneuse vidéo.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Attribut de configuration pour la visionneuse vidéo.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span></span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage de clic/clic pour activer/désactiver la lecture/la mise en pause. La valeur <span class="codeph"> none</span> désactive le clic/clic pour lire/mettre en pause. Si elle est définie sur <span class="codeph"> playPause</span>, un clic sur la vidéo fait basculer la lecture vers la mise en pause. Sur certains périphériques, vous pouvez utiliser des contrôles natifs. Dans ce cas, le comportement <span class="codeph"> singleclick</span> est désactivé. </p> </td> 
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

