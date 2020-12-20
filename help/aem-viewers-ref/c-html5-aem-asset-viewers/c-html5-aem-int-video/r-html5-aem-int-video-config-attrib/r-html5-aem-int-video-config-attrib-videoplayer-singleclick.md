---
description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-description: Attribut de configuration pour la visionneuse de vidéos interactive.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic media
uuid: 5b387eb6-1e09-4506-beea-3f1cf337cb9d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Attribut de configuration pour la visionneuse de vidéos interactive.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage de clic/clic unique pour activer/désactiver la lecture/la pause. La définition de <span class="codeph"> none</span> désactive la lecture/mise en pause d’un seul clic/clic. Si elle est définie sur <span class="codeph"> playPause</span>, cliquez sur la vidéo pour basculer entre la lecture et la mise en pause. Sur certains périphériques, vous pouvez utiliser des contrôles natifs. Dans ce cas, un comportement <span class="codeph"> singleclick</span> est désactivé. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

