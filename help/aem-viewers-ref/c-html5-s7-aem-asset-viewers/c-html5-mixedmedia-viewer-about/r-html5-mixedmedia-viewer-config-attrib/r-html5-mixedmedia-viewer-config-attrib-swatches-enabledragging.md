---
description: 'null'
seo-description: 'null'
seo-title: Nuancier.activation du glissement
solution: Experience Manager
title: Nuancier.activation du glissement
topic: Dynamic media
uuid: f676b0b1-2ce0-4409-8db6-ce162b03053b
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

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,0.5`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enabledragging=0`
