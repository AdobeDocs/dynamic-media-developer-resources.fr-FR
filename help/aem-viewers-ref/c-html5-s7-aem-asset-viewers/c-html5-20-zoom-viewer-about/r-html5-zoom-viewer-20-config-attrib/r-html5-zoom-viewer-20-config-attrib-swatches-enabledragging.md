---
description: 'null'
seo-description: 'null'
seo-title: Nuancier.activation du glissement
solution: Experience Manager
title: Nuancier.activation du glissement
topic: Dynamic media
uuid: 0bfd7275-59c7-446f-b056-93ed79352462
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Nuancier.activation du glissement{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

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

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enabledragging=0`
