---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 9b69f6d7-b7a1-42c6-98d7-80952b7f8b31
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Active ou désactive la possibilité, pour un utilisateur, de faire défiler les échantillons à l’aide de la souris ou d’un toucher </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> <span class="varname"> overdragvalue </span> </span> </p> </td> 
   <td> <p> Fonctions comprises dans la plage de <span class="codeph"> 0-1 </span>. Il s'agit d'une valeur <span class="codeph"> de </span> % pour un mouvement dans le mauvais sens de la vitesse réelle. S’il est défini sur <span class="codeph"> 1 </span>, il se déplace avec la souris. S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas du tout d’avancer dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`1,0.5`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`enabledragging=0`
