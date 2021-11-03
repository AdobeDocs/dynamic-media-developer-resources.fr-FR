---
title: SmartCropVideoPlayer.playback
description: Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressif</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. When <span class="codeph"> auto</span> est définie sur , sur la plupart des navigateurs de bureau et tous les appareils iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS. Il revient à la lecture progressive de HTML5 sur certains systèmes tels qu’Internet Explorer et Android™. </p> <p>If <span class="codeph"> progressif</span> est spécifiée, la visionneuse ne repose que sur la lecture HTML5 comme prise en charge en mode natif par les navigateurs et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en modes automatique et progressif, consultez le Guide de l’utilisateur du SDK de la visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

Ignoré lorsque la visionneuse fonctionne avec une vidéo externe. Voir [Prise en charge des vidéos externes]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
