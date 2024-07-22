---
title: Swatches.align
description: Swatches.align
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 4f25112b-9e51-4a0e-9500-1b5ab0f4de87
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Swatches.align{#swatches-align}

`[Swatches.|<containerId>_swatches.]align=left|center|right,top|center|bottom`

Indique l’alignement interne (ancrage) du conteneur d’échantillons dans la zone du composant. Dans les nuanciers, le conteneur de miniatures interne est dimensionné de sorte que seul un nombre entier d’échantillons s’affiche. Par conséquent, il existe une marge intérieure entre le conteneur interne et les limites de composants externes. Cette commande indique comment le conteneur d’échantillons internes est positionné dans le composant.

<table id="table_58D88FF5F83A4ABA928695B5AFF97354"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> left|center|right</span> </p> </td> 
   <td> <p> Définit l’alignement des échantillons horizontaux. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><span class="codeph"> top|center|bottom</span> </p> </td> 
   <td> <p> Définit l’alignement des échantillons verticaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`center,center`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`align=left,top`
