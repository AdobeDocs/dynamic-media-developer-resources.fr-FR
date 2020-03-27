---
description: 'null'
seo-description: 'null'
seo-title: Nuancier.activation du glissement
solution: Experience Manager
title: Nuancier.activation du glissement
topic: Dynamic media
uuid: 2b5dff77-25e3-42cd-bdae-0a96f04f881e
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

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
