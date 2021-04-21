---
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
title: Video360Player.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: dfb44ed5-5f4f-4a2c-a3b4-d49502556399
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 9%

---

# Video360Player.singleclick{#video-player-singleclick}

Attribut de configuration pour la visionneuse Video360.

`[Video360Player.|<containerId>_video360Player.]singleclick=none|playPause`

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
