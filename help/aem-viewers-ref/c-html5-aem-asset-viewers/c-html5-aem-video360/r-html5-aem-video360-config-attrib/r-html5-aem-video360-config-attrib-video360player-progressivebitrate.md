---
description: Attribut de configuration pour la visionneuse Video360.
solution: Experience Manager
title: Video360Player.progressivebitrate
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 7%

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
