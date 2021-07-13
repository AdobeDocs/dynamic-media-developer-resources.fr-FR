---
description: Attribut de configuration de la visionneuse de vidéos interactives.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Visionneuses,SDK/API,Vidéos interactives
role: Developer,User
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attribut de configuration de la visionneuse de vidéos interactives.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage d’un clic/d’un clic pour activer/désactiver la lecture/la pause. La définition de sur <span class="codeph"> none</span> désactive la fonction cliquer/appuyer une seule fois pour lancer la lecture/la pause. Si elle est définie sur <span class="codeph"> playPause</span>, un clic sur la vidéo fait basculer entre la lecture et la mise en pause de la vidéo. Sur certains périphériques, vous pouvez utiliser des contrôles natifs. Dans ce cas, un comportement <span class="codeph"> singleclick</span> est désactivé. </p> </td> 
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
