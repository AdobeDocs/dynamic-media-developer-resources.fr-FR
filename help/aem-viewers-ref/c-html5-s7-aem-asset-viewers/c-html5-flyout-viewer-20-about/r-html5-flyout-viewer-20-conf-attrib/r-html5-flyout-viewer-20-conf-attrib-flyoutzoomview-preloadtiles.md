---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
uuid: e73f9d5d-4b7a-4a6b-8d0f-a5e588dc00c9
feature: Dynamic Media Classic, Visionneuses, SDK/API, Fenêtre déroulante
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '70'
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

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`preloadtiles=1`
