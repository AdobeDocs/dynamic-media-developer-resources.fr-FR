---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 39cb629a-3940-4206-91cd-fe9a9f4d9f75
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 6%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`duration`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade</span> </p> </td> 
   <td colname="col2"> <p> </p> <p> Indique le type d’effet appliqué à la vue principale lors du changement de ressource. </p> <p><span class="codeph"> none</span> signifie aucune transition, le changement d’affichage principal se produit instantanément. </p> <p><span class="codeph"> fade</span> active une transition de fondu croisé lorsque l’ancienne image s’estompe et que la nouvelle image s’estompe </p> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p> Nombre de secondes nécessaires à la réalisation de l’animation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

Aucune

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`frametransition=fade,1`
