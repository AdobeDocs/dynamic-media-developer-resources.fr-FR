---
description: permet de configurer la manière dont le composant récupère les nouvelles images pour le principal et le  de fenêtre déroulante lors du redimensionnement.
seo-description: permet de configurer la manière dont le composant récupère les nouvelles images pour le principal et le  de fenêtre déroulante lors du redimensionnement.
seo-title: FlyoutZoomView.imagereload
solution: Experience Manager
title: FlyoutZoomView.imagereload
topic: Dynamic media
uuid: 5cded4cb-7b02-47da-9e2d-b236548cc61d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

permet de configurer la manière dont le composant récupère les nouvelles images pour le principal et le  de fenêtre déroulante lors du redimensionnement.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`largeur`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>Lorsqu’il est défini sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement et la résolution de l’image dans le de fenêtre déroulante ne change pas. </p> <p>Lorsqu’il est défini sur <span class="codeph"> 1, </span> vous pouvez spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans le principal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt, <span class="varname"> width </span>[; <span class="varname"> width </span>] </span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur de l’image chargée dans le  principal du. Le composant utilisera toujours la meilleure taille d’ajustement pour la charge initiale. Une fois redimensionné, l’image dans le principal est toujours téléchargée avec la largeur égale au point d’arrêt le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
