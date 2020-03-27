---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 98a84ba1-4b89-424a-ac2e-4a59af33cec0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`largeur`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> permet de configurer la manière dont le composant récupère les nouvelles images pour le principal et le  de fenêtre déroulante lors du redimensionnement. </p> <p>Défini sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement et la résolution de l’image dans le de fenêtre déroulante ne change pas. </p> <p>La valeur <span class="codeph"> 1 </span> permet de spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans le  principal du. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt, <span class="varname"> width </span>[; <span class="varname"> largeur </span></span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur de l’image chargée dans le  principal du. </p> <p>Le composant utilise toujours la meilleure taille d’ajustement pour la charge initiale. Une fois redimensionnée, elle permet de s’assurer que l’image du  principal est toujours téléchargée à l’aide de la largeur égale au point d’arrêt le plus grand, puis réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
