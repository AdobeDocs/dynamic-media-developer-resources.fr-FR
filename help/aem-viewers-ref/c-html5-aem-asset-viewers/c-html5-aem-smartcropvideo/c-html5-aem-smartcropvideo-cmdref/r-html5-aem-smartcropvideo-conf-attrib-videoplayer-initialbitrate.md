---
title: SmartCropVideoPlayer.initialbitrate
description: Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4fc4fefa-b094-4e2e-b8ec-a439f8a1a56c
TQID: 'https://experienceleague.adobe.com/28EPvFEtw-wS3EhTuDHpTWO1wksSmLnrKfwNJVRkFk4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%
---
# SmartCropVideoPlayer.initialbitrate{#smartcropvideoplayer-initialbitrate}

Attribut de configuration de la visionneuse de vidéos.

` [SmartCropVideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> </span> de la valeur <span class="codeph"> </p> </td> 
   <td colname="col2"> <p>Définit le débit vidéo (en kilobits par seconde ou kbit/s) utilisé pour la lecture initiale de la vidéo sur les ordinateurs de bureau. </p> <p>Si cette valeur de débit n’existe pas dans la visionneuse de vidéos adaptative, le lecteur vidéo lance la vidéo qui a le débit le plus faible suivant. </p> <p>S’il est défini sur <span class="codeph"> 0 </span>, le lecteur vidéo démarre à partir du débit le plus faible possible. Applicable uniquement aux systèmes qui ne prennent pas en charge nativement la vidéo HTML5 HLS (qui sont des navigateurs Firefox, Chrome et Internet Explorer 11 sous Windows 10) et lorsque le mode de lecture est défini sur <span class="codeph"> le </span> automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
