---
description: Attribut de configuration pour la visionneuse Video360.
seo-description: Attribut de configuration pour la visionneuse Video360.
seo-title: Video360Player.singleclick
solution: Experience Manager
title: Video360Player.singleclick
topic: Dynamic media
uuid: 2972405c-5c89-45d0-a542-19c7463901b4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 12%

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

