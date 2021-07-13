---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: b156d3f4-c4d3-45fe-b3d3-b7ed38f6eb4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 4%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Indique (en Kbits par seconde ou en Kbits/s) le débit vidéo souhaité à lire à partir d’une visionneuse de vidéos adaptative au cas où le système actuel ne prendrait pas en charge la lecture de vidéo adaptative. </p> <p>Le composant récupère le flux vidéo avec le débit le plus proche possible (mais ne dépassant pas) par rapport à la valeur spécifiée. Si tous les flux vidéo de la visionneuse de vidéos adaptative ont une qualité supérieure à la valeur spécifiée, la logique choisit le débit avec la qualité la plus faible. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
