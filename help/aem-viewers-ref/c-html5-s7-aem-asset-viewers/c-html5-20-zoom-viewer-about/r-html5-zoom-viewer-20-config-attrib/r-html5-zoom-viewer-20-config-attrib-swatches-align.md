---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 3cb91483-de8c-4d5c-9b46-7026c5001f3a
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Spécifie l’alignement interne (ancrage) du conteneur d’échantillons dans la zone du composant. Dans les échantillons, le conteneur de vignettes interne est dimensionné de sorte que seul un nombre entier d’échantillons soit affiché. Par conséquent, il existe un certain remplissage entre les limites du conteneur interne et du composant externe. Cette commande indique la position du conteneur d’échantillons internes à l’intérieur du composant.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> gauche|centre|droite</span> </p> </td> 
   <td> <p> Définit l’alignement des échantillons horizontaux. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> haut|centre|bas</span> </p> </td> 
   <td> <p> Définit l’alignement des échantillons verticaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`center,center`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`align=left,top`
