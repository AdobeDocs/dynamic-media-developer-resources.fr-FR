---
title: FlyoutZoomView.imagereload
description: Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la vue déroulante lors du redimensionnement.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1bb57c89-4ceb-40d6-8054-d51c1573431c
TQID: 'https://experienceleague.adobe.com/vyA-GdKo06kVi3jO6wlBIyov3XvKVo1vwPj3mzqyoc4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 3%

---

# FlyoutZoomView.imagereload{#flyoutzoomview-imagereload}

Configure la manière dont le composant récupère de nouvelles images pour la vue principale et la vue déroulante lors du redimensionnement.

` [FlyoutZoomView.|<containerId>_flyout.]imagereload=0|1[,breakpoint, *`width`*[; *`width`*]]`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p>Lorsque la valeur est définie sur <span class="codeph"> 0 </span>, le composant ne charge pas les nouvelles images lors du redimensionnement et la résolution de l’image dans la vue déroulante ne change pas. </p> <p>Défini sur <span class="codeph"> 1 </span> permet de définir un ou plusieurs points d’arrêt de largeur pour l’image chargée dans la vue principale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> point d'arrêt, <span class="varname"> largeur </span>[; <span class="varname"> largeur </span>] </span> </p> </td> 
   <td colname="col2"> <p>Points d’arrêt de largeur pour l’image chargée en mode principal. Le composant utilise toujours la meilleure taille pour la charge initiale. Après le redimensionnement, il garantit que l’image en mode principal est toujours téléchargée avec une largeur égale au point d’arrêt le plus proche et réduit sur le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`0`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`imagereload=1,breakpoint,200;400;800;1600`
