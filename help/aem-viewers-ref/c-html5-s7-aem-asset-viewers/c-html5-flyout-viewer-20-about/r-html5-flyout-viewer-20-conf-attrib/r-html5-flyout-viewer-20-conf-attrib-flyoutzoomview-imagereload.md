---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 483fa64b-5196-4477-8ea6-0f32c6557f72
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *` `*[; *`width width`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configure la façon dont le composant récupère les nouvelles images pour la vue principale et la vue déroulante lors du redimensionnement. </p> <p>Lorsqu’il est défini sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement ; la résolution de l’image dans la vue déroulante ne change pas. </p> <p>La définition sur <span class="codeph"> 1 </span> vous permet de spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">point d’arrêt, <span class="varname"> width </span>[ ; width ]<span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> Points d’arrêt de largeur de l’image chargée dans la vue principale. Le composant utilise toujours la meilleure taille d’ajustement pour la charge initiale. Après le redimensionnement, il garantit que l’image dans la vue principale est toujours téléchargée avec la largeur égale au point d’arrêt le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
