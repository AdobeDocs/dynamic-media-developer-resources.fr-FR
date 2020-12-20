---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
topic: Dynamic media
uuid: c9989916-d0f3-4268-932a-e12c693f5b74
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 10%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Définissez ce paramètre sur <span class="codeph"> 1</span> pour activer le préchargement de l’image agrandie. </p> <p>Définissez ce paramètre sur <span class="codeph"> 0</span> pour charger l’image de zoom de manière incrémentielle, selon les besoins. </p> <p> <p>Remarque :  Sachez que si vous activez cette option, elle peut entraîner une utilisation de bande passante beaucoup plus élevée, car l’image agrandie doit être chargée dans son intégralité, même si l’utilisateur n’effectue aucune action de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`preloadtiles=1`
