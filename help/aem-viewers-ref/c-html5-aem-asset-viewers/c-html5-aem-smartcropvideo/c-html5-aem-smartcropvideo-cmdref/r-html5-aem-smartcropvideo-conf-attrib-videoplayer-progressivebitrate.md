---
title: SmartCropVideoPlayer.progressivebitrate
description: Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 25e3e7e9-0979-472c-a589-aaf0e221b885
TQID: 'https://experienceleague.adobe.com/HSShyhUx64vEYIAuInb1sRH5UAdknbAkQWFjYv4yvxo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 3%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valeur </span> </p> </td> 
   <td colname="col2"> <p> Indique le débit vidéo souhaité (en kilobits par seconde ou kbit/s) à lire à partir d’une visionneuse de vidéos adaptative au cas où le système actuel ne prend pas en charge la lecture de vidéo adaptative. </p> <p>Le composant sélectionne le flux vidéo ayant le débit le plus proche possible (sans toutefois le dépasser) de la valeur spécifiée. Si tous les flux vidéo de la visionneuse de vidéos adaptative ont une qualité supérieure à la valeur spécifiée, la logique choisit le débit avec la qualité la plus faible. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-f42369774e2740dcb399626a0e4e930e}

Facultatif.

## Par défaut {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Exemple {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
