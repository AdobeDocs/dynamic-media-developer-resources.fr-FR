---
title: FlyoutZoomView.imagereload
description: Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la fenêtre déroulante lors du redimensionnement.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 2%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la fenêtre déroulante lors du redimensionnement.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Lorsqu’il est défini sur <span class="codeph"> 0 </span>, le composant ne charge pas de nouvelles images lors du redimensionnement, et la résolution de l’image dans la vue déroulante ne change pas. </p> <p>Lorsque la valeur est définie sur <span class="codeph"> 1 </span>, vous pouvez spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt, <span class="varname"> largeur </span>[; <span class="varname"> largeur </span>] </span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur pour l’image chargée dans la vue principale. Le composant utilise toujours la meilleure taille d’ajustement pour la charge initiale. Une fois redimensionné, l’image dans la vue principale est toujours téléchargée avec la largeur égale au point d’arrêt le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
