---
description: Attribut de configuration pour la visionneuse Video360.
seo-description: Attribut de configuration pour la visionneuse Video360.
seo-title: Video360Player.progressivebitrate
solution: Experience Manager
title: Video360Player.progressivebitrate
topic: Dynamic media
uuid: 438c18d7-e7ac-4834-8445-def590264448
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 9%

---


# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Attribut de configuration pour la visionneuse Video360.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Indique, en kbits/s (ou kbits/s), le débit vidéo souhaité à lire à partir d’une visionneuse de vidéos adaptative au cas où le système actuel ne prendrait pas en charge la lecture de vidéo adaptative. </p> <p>Le composant récupère le flux vidéo avec le débit le plus proche possible (mais n’excédant pas) par rapport à la valeur spécifiée. Si la qualité de tous les flux vidéo de la visionneuse de vidéos adaptative est supérieure à la valeur spécifiée, la logique choisit le débit avec la qualité la plus basse. </p> </td> 
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

