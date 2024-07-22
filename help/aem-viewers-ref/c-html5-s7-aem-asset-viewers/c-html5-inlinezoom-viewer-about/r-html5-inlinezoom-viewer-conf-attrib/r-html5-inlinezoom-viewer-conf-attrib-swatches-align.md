---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: d9db34f3-66df-45c2-9727-bdcdf09773db
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

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`center,center`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`align=left,top`
