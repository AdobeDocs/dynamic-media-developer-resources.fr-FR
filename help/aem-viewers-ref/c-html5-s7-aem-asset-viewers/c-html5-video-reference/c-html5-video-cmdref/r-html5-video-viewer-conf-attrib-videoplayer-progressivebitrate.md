---
description: Attribut de configuration pour la visionneuse vidéo.
seo-description: Attribut de configuration pour la visionneuse vidéo.
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic media
uuid: 2e911d35-155e-4afa-aede-52e9d00ae211
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Attribut de configuration pour la visionneuse vidéo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Indique (en kbits/s ou kbits/s) le débit vidéo souhaité à lire à partir d’une visionneuse de vidéos adaptative au cas où le système actuel ne prendrait pas en charge la lecture de vidéos adaptatives. </p> <p>Le composant récupère le flux vidéo avec le débit le plus proche possible (mais n’excédant pas) de la valeur spécifiée. Si la qualité de tous les flux vidéo de la visionneuse de vidéos adaptative est supérieure à la valeur spécifiée, la logique choisit le débit avec la qualité la plus faible. </p> </td> 
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

