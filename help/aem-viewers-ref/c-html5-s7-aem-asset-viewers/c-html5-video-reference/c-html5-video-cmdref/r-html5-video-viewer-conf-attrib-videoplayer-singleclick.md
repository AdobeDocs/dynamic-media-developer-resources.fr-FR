---
title: VideoPlayer.singleclick
description: Attribut de configuration de la visionneuse de vidéos.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
TQID: 'https://experienceleague.adobe.com/RH1L9ADikh3LiDMwfqDdrGOZ7L08nRyFgIly2yCKZf4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 4%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Attribut de configuration de la visionneuse de vidéos.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> aucun|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configure le mappage d’un clic/appui unique pour activer/désactiver la lecture/pause. Si vous définissez sur <span class="codeph"> aucun</span> désactivez la lecture/mise en pause en un seul clic ou en appuyant dessus. Si vous définissez sur <span class="codeph"> playPause</span>, cliquez sur la vidéo pour basculer entre la lecture et la mise en pause de la vidéo. Sur certains appareils, vous pouvez utiliser des contrôles natifs. Dans ce cas, <span class="codeph"> comportement de simple clic</span> est désactivé. </p> </td> 
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
