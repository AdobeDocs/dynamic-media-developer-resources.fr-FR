---
title: FlyoutZoomView.imagereload
description: FlyoutZoomView.imagereload
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 84dd1e40-2ab8-4356-9eff-8766432b539b
TQID: 'https://experienceleague.adobe.com/utzPqD5UMx7TnJK8FvqflzoSjOWGVaGXhKlviY1U9xQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 4%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_7DA232CB62134078B788B9AB1452F363"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la vue déroulante lors du redimensionnement. </p> <p>Définissez sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement et la résolution de l’image dans la vue déroulante ne change pas. </p> <p>Défini sur <span class="codeph"> 1 </span> permet de définir un ou plusieurs points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d’arrêt, largeur <span class="varname"> </span> ; largeur <span class="varname"> </span> </span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur pour l’image chargée dans l’affichage principal. </p> <p>Le composant utilise toujours la taille la plus adaptée pour la charge initiale. Après le redimensionnement, cela garantit que l’image de la vue principale est toujours téléchargée à l’aide de la largeur égale au point d’arrêt le plus grand le plus proche et réduite sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,breakpoint,300;600;1200`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`imagereload=1,breakpoint,200;400;800;1600`
