---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,User
exl-id: 041df5c7-9391-4dde-8988-a83272c7c438
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Définissez cette variable sur <span class="codeph"> 1</span> pour activer le préchargement de l’image agrandie. </p> <p>Définissez cette variable sur <span class="codeph"> 0</span> pour charger l’image de zoom de manière incrémentielle, selon les besoins. </p> <p> <p>Remarque :  N’oubliez pas que si vous activez cette option, l’utilisation de la bande passante peut être considérablement plus élevée, car l’image agrandie doit être chargée dans son intégralité, même si l’utilisateur n’effectue aucune action de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
