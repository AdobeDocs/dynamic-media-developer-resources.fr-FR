---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom intégré
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Définissez cette variable sur <span class="codeph"> 1</span> pour activer le préchargement de l’image agrandie ou sur <span class="codeph"> 0</span> pour charger l’image de zoom par incréments, selon les besoins. </p> <p> <p>Remarque :  Si vous activez cette option, l’utilisation de la bande passante risque d’être considérablement plus élevée. L’image agrandie est chargée dans son intégralité, même si l’utilisateur ne lance pas d’action de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
