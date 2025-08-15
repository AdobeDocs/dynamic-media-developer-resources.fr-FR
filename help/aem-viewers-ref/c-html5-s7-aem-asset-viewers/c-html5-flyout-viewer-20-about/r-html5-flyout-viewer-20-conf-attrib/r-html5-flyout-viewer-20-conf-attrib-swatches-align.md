---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 300bbee8-29f1-444d-bf98-42aeb9c5017b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Spécifie l’alignement interne (ancrage) du conteneur d’échantillons dans la zone de composant. Dans les échantillons, le conteneur de vignettes interne est dimensionné de sorte que seul un nombre entier d’échantillons soit affiché. Par conséquent, il existe un certain remplissage entre le conteneur interne et les limites du composant externe. Cette commande indique la position du conteneur d’échantillons internes à l’intérieur du composant.

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> gauche|centre|droite</span> </p> </td> 
   <td colname="col2"> <p> Définit l’alignement horizontal des échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> haut|centre|bas</span> </p> </td> 
   <td colname="col2"> <p> Définit l’alignement des échantillons verticaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`center,center`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`align=left,top`
