---
title: ThumbnailGridView.enabledragging
description: ThumbnailGridView.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e3615e82-d8f0-427e-ab32-f7d0f2b6cbf3
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Permet ou désactive la possibilité pour un utilisateur de faire défiler les échantillons avec la souris ou à l’aide de mouvements tactiles. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Fonctions comprises dans la plage <span class="codeph"> 0-1 </span>. Il s’agit d’une valeur <span class="codeph"> % </span> pour le mouvement dans la mauvaise direction de la vitesse réelle. Si elle est définie sur <span class="codeph"> 1 </span>, elle se déplace avec la souris. Si elle est définie sur <span class="codeph"> 0 </span>, elle ne vous permet pas du tout de vous diriger dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-831c23dea82449bfa50fd155bea365b7}

Facultatif.

## Par défaut {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## Exemple {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
