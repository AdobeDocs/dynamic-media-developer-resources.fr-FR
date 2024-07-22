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

Indique l’alignement interne (ancrage) du conteneur d’échantillons dans la zone du composant. Dans les nuanciers, le conteneur de miniatures interne est dimensionné de sorte que seul un nombre entier d’échantillons s’affiche. Par conséquent, il existe une marge intérieure entre le conteneur interne et les limites du composant externe. Cette commande spécifie le mode de positionnement du conteneur d’échantillons internes dans le composant.

<table id="table_33CC037517964DA89EE0C005BB6B32BB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> left|center|right</span> </p> </td> 
   <td colname="col2"> <p> Définit l’alignement horizontal des échantillons. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
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
