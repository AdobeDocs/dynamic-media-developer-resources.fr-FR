---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 1de87e2f-5cb9-406a-96bc-3486c2592951
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`largeur`*]]`

<table id="table_42CA0074AD7C4F0D9FC81E9FCB0591C0"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> permet de configurer la manière dont le composant récupère les nouvelles images pour le principal et le  de fenêtre déroulante lors du redimensionnement. </p> <p>Lorsqu’il est défini sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement ; la résolution de l’image dans le de fenêtre déroulante  ne change pas. </p> <p>La valeur <span class="codeph"> 1 </span> permet de spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans le  principal du. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt, <span class="varname"> width </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p> Points d’arrêt de largeur de l’image chargée dans le  principal du. Le composant utilise toujours la meilleure taille d’ajustement pour la charge initiale. Après le redimensionnement, il s’assure que l’image du principal est toujours téléchargée avec la largeur égale au point d’arrêt le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`0`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`imagereload=1,breakpoint,200;400;800;1600`
