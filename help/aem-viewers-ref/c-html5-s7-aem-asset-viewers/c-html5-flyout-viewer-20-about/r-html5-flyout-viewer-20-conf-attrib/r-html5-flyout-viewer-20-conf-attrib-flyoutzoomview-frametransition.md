---
title: FlyoutZoomView.frametransition
description: FlyoutZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 0b0a88a0-d736-4ab8-a25f-15d1689b0a48
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# FlyoutZoomView.frametransition{#flyoutzoomview-frametransition}

` [FlyoutZoomView.|<containerId>_flyout.]frametransition=none|fade[, *`durée`*]`

<table id="table_FC34B37AACFB4E92A37E1D2D93D5F0D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Aucun|fondu</span> </p> </td> 
   <td colname="col2"> <p> Spécifie le type d’effet appliqué à la vue principale lors de la modification d’actif. Le <span class="codeph"> none</span> signifie pas de transition, le changement de vue principale se produit instantanément. Le <span class="codeph"> fondu</span> active la transition en fondu enchaîné où l’ancienne image s’estompe et la nouvelle image apparaît en fondu au sort </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> durée</span></span> </p> </td> 
   <td colname="col2"> <p> Durée de l’animation en secondes. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

Aucune

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`frametransition=fade,1`
