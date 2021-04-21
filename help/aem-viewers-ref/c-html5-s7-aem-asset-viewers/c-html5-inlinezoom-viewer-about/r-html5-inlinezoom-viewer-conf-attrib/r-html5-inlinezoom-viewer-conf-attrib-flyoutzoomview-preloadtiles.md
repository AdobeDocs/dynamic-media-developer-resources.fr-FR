---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Définissez ce paramètre sur <span class="codeph"> 1</span> pour activer le préchargement de l’image agrandie ou sur <span class="codeph"> 0</span> pour charger l’image de zoom par incréments, si nécessaire. </p> <p> <p>Remarque :  Si vous activez cette option, elle peut entraîner une utilisation beaucoup plus élevée de la bande passante. L’image agrandie est chargée dans son intégralité, même si l’utilisateur ne lance pas d’action de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
