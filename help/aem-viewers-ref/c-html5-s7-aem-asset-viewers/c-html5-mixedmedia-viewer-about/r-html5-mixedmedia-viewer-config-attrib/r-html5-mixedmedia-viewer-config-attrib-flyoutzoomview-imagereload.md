---
description: Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la fenêtre déroulante lors du redimensionnement.
solution: Experience Manager
title: FlyoutZoomView.imagereload
feature: Dynamic Media Classic,Visionneuses,SDK/API,Visionneuses de médias mixtes
role: Developer,Business Practitioner
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la fenêtre déroulante lors du redimensionnement.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *``*[; *`largeur`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p>Lorsqu’il est défini sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement, et la résolution de l’image dans la vue déroulante ne change pas. </p> <p>Lorsqu’elle est définie sur <span class="codeph"> 1 </span> , vous permet de spécifier un ou plusieurs points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt,  <span class="varname"> largeur  </span>[;  <span class="varname"> width  </span>]  </span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur pour l’image chargée dans la vue principale. Le composant utilisera toujours la meilleure taille pour la charge initiale. Une fois redimensionné, l’image de la vue principale est toujours téléchargée avec la largeur égale au point d’arrêt le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
