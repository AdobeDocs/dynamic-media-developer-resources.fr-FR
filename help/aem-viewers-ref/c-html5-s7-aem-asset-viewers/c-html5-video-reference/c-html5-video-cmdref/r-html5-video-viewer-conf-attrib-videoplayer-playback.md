---
description: Attribut de configuration pour la visionneuse de vidéos.
solution: Experience Manager
title: VideoPlayer.playback
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# VideoPlayer.playback{#videoplayer-playback}

Attribut de configuration pour la visionneuse de vidéos.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. Lorsque <span class="codeph"> auto</span> est défini, sur la plupart des navigateurs de bureau et sur tous les périphériques iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS. Il revient à la lecture HTML5 progressive sur certains systèmes tels que l’ancien Internet Explorer et Android. </p> <p>Si <span class="codeph"> progressive</span> est spécifié, la visionneuse ne s’appuie que sur la lecture HTML5, prise en charge en mode natif par les navigateurs, et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en mode automatique et progressif, consultez le Guide de l’utilisateur du SDK de la visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

Ignoré lorsque la visionneuse fonctionne avec une vidéo externe. Voir [Prise en charge des vidéos externes](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

