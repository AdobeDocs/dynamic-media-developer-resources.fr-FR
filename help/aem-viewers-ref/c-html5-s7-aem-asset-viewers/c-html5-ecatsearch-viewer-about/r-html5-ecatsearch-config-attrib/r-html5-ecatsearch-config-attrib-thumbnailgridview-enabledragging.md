---
description: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 011ef772-6760-4794-819e-2a822fbae1b5
TQID: 'https://experienceleague.adobe.com/R-8C-obmM18dPSWcLrekSvAzSRRTrthSDePpybEcCOc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 80
ht-degree: 6%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

[!DNL `[ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`]

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Active ou désactive la possibilité, pour un utilisateur, de faire défiler les échantillons à l’aide de la souris ou d’un toucher </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Fonctions comprises dans la plage de </span> 0-1 <span class="codeph">. Il s'agit d'une valeur </span> de <span class="codeph"> % pour un mouvement dans le mauvais sens de la vitesse réelle. S’il est défini sur <span class="codeph"> 1 </span>, il se déplace avec la souris. S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas du tout d’avancer dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-831c23dea82449bfa50fd155bea365b7}

Facultatif.

## Par défaut {#section-464be2db89f34516ad93f32f7783d2b0}

[!DNL `1,0.5`]

## Exemple {#section-e67c8807762e471bb03d6a8fb20e19d4}

[!DNL `enabledragging=0`]
