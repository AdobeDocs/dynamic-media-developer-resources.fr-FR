---
title: Swatches.enabledragging
description: Swatches.enabledragging
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7ffdc886-5631-429f-84b4-4b32b715713d
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Swatches.enabledragging{#swatches-enabledragging}

` [Swatches.|<containerId>_swatches.]enabledragging=0|1[, *`Valeur de surglissement`*]`

<table id="table_B1363BFD20204093AAB326A1AB503B93"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td> <p> Permet ou désactive la possibilité pour un utilisateur de faire défiler les échantillons avec la souris ou en utilisant des gestes tactiles </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> Valeur de surglissement </span> </span> </p> </td> 
   <td> <p> Fonctionne dans la <span class="codeph"> plage 0-1 </span> . Il s’agit d’une <span class="codeph"> valeur en % </span> pour le mouvement dans la mauvaise direction de la vitesse réelle. S’il est défini sur <span class="codeph"> 1 </span>, il se déplace avec la souris. S’il est défini sur <span class="codeph"> 0 </span>, il ne vous permet pas du tout de vous déplacer dans la mauvaise direction. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`1,0.5`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`enabledragging=0`
