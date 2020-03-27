---
description: 'null'
seo-description: 'null'
seo-title: ThumbnailGridView.enabledragging
solution: Experience Manager
title: ThumbnailGridView.enabledragging
topic: Dynamic media
uuid: d7a12c2e-b50e-473e-9406-8ef0541e38c4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ThumbnailGridView.enabledragging{#thumbnailgridview-enabledragging}

` [ThumbnailGridView.|<containerId>_gridView.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td> <p> Active ou désactive la possibilité pour un utilisateur de faire défiler les échantillons avec une souris ou en utilisant des mouvements tactiles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span></span> </p> </td> 
   <td> <p> Fonctions dans la plage <span class="codeph"> 0-1 </span> . Il s'agit d'une valeur de <span class="codeph"> % </span> pour le mouvement dans la mauvaise direction de la vitesse réelle. S’il est défini sur <span class="codeph"> 1 </span>, il bouge avec la souris. S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas du tout de vous diriger dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-831c23dea82449bfa50fd155bea365b7}

Facultatif.

## Par défaut {#section-464be2db89f34516ad93f32f7783d2b0}

`1,0.5`

## Exemple {#section-e67c8807762e471bb03d6a8fb20e19d4}

`enabledragging=0`
