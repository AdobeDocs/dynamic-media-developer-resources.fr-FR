---
title: VideoPlayer.playback
description: Attribut de configuration pour la visionneuse vidéo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# VideoPlayer.playback{#videoplayer-playback}

Attribut de configuration pour la visionneuse vidéo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Définit le type de lecture utilisé par la visionneuse. Lorsque <span class="codeph"> l’option automatique</span> est définie, sur la plupart des navigateurs de bureau et tous les appareils iOS, la visionneuse utilise la vidéo en flux continu HTML5 au format HLS. Il revient à la lecture HTML5 progressive sur certains systèmes comme Internet Explorer et Android™. </p> <p>Si <span class="codeph"> progressive</span> est spécifiée, la visionneuse s’appuie uniquement sur la lecture HTML5 telle qu’elle est prise en charge nativement par les navigateurs et lit la vidéo progressivement sur tous les systèmes. </p> <p>Pour plus d’informations sur la sélection de la lecture en mode automatique et progressif, consultez le Guide de l’utilisateur du Kit de développement logiciel (SDK) de la visionneuse. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

Ignoré lorsque la visionneuse utilise une vidéo externe. Voir Prise en [charge](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) vidéo externe.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
