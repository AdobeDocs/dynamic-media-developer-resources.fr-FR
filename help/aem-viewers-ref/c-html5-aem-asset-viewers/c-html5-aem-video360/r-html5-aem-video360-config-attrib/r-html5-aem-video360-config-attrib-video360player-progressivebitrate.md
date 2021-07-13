---
description: Attribut de configuration de la visionneuse Video360.
solution: Experience Manager
title: Video360Player.progressivebitrate
feature: Dynamic Media Classic,Visionneuses,SDK/API,vidéo 360 VR
role: Developer,User
exl-id: a253ef01-19ae-4de4-a4fc-b10b28e72c00
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 7%

---

# Video360Player.progressivebitrate{#video-player-progressivebitrate}

Attribut de configuration de la visionneuse Video360.

` [Video360Player.|<containerId>_video360Player.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Indique, en Kbits/s (ou Kbits/s), le débit vidéo souhaité à lire à partir d’une visionneuse de vidéos adaptative au cas où le système actuel ne prendrait pas en charge la lecture de vidéos adaptatives. </p> <p>Le composant récupère le flux vidéo avec le débit le plus proche possible (mais ne dépassant pas) par rapport à la valeur spécifiée. Si tous les flux vidéo de la visionneuse de vidéos adaptative ont une qualité supérieure à la valeur spécifiée, la logique choisit le débit avec la qualité la plus faible. </p> </td> 
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
