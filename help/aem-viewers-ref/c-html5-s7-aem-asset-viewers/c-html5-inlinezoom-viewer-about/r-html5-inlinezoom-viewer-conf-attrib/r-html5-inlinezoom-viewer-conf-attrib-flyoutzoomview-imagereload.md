---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la fenêtre déroulante lors du redimensionnement. </p> <p>Définissez sur . <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement, et la résolution de l’image dans la vue déroulante ne change pas. </p> <p>Définissez sur . <span class="codeph"> 1 </span> permet de spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt, <span class="varname"> width </span>; <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> <p>Le composant utilise toujours la meilleure taille d’ajustement pour la charge initiale. Une fois redimensionné, l’image de la vue principale est toujours téléchargée à l’aide de la largeur égale au point d’arrêt le plus grand le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
