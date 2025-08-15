---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`width width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configure la façon dont le composant récupère les nouvelles images pour la vue principale et la vue déroulante lors du redimensionnement. </p> <p>Défini sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement et la résolution de l’image dans la vue déroulante ne change pas. </p> <p>La valeur 1 <span class="codeph"> </span> vous permet de spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt, <span class="varname"> largeur </span>; <span class="varname"> largeur </span> </span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur de l’image chargée dans la vue principale. </p> <p>Le composant utilise toujours la meilleure taille d’ajustement pour la charge initiale. Après le redimensionnement, il garantit que l’image dans la vue principale est toujours téléchargée en utilisant la largeur égale au point d’arrêt le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
