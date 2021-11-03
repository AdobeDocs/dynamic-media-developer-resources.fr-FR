---
description: Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.
solution: Experience Manager
title: SmartCropVideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Attribut de configuration de la visionneuse de vidéos avec recadrage intelligent.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Indique (en Kbits par seconde ou en Kbits/s) le débit vidéo souhaité à lire à partir d’une visionneuse de vidéos adaptative au cas où le système actuel ne prendrait pas en charge la lecture de vidéo adaptative. </p> <p>Le composant récupère le flux vidéo avec le débit le plus proche possible (mais ne dépassant pas) par rapport à la valeur spécifiée. Si tous les flux vidéo de la visionneuse de vidéos adaptative ont une qualité supérieure à la valeur spécifiée, la logique choisit le débit avec la qualité la plus faible. </p> </td> 
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
