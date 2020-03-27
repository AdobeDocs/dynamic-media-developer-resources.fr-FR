---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.highlightmode
solution: Experience Manager
title: FlyoutZoomView.highlightmode
topic: Dynamic media
uuid: 397c1af0-f806-4555-83fa-ec7548b59a60
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`démonstration`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> surligner|curseur </span> </p> </td> 
   <td colname="col2"> <p> Indique le type de cadre de navigation à utiliser. Lorsqu’il est défini sur <span class="codeph"> cursor </span>, le composant utilise un curseur de référence de taille fixe. Il est possible d'avoir différents graphiques de curseur pour les systèmes de bureau et les périphériques tactiles, ceci est contrôlé avec la classe <span class="codeph"> .s7cursor </span> CSS et <span class="codeph"> =mouse|touch </span> attribute selector. Sur les systèmes de bureau, un point d’ancrage est défini au milieu de la zone du curseur, tandis que sur les périphériques tactiles, l’ancre est située au centre inférieur du curseur. Lorsqu’il est défini sur <span class="codeph"> surligner </span>, le composant utilise un cadre de navigation de taille variable ; la taille et la forme du cadre dépendent du facteur de zoom et de la taille du  de fenêtre déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> démonstration </span></span> </p> </td> 
   <td colname="col2"> <p> Définit la durée (en secondes) pendant laquelle la mise en surbrillance ou le curseur s’estompe une fois activé par l’utilisateur. Le fondu d’entrée est appliqué uniquement sur les périphériques tactiles ; sur les systèmes de bureau, il est ignoré par le composant. </p> <p>Le fondu dans s’applique aux éléments de l’interface utilisateur suivants : cadre de surbrillance, curseur fixe, incrustation (au cas où le paramètre <span class="codeph"> d’incrustation </span> serait défini sur <span class="codeph"> 1 </span>). L’animation de la  Fenêtre déroulante ne commence qu’une fois le surlignage/le fondu du curseur dans l’animation terminée. Il n'y a pas d'animation en fondu. Lorsque l’utilisateur désactive la fenêtre déroulante, les éléments correspondants de l’interface (curseur, mise en surbrillance et recouvrement) se masquent instantanément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Contrôle le positionnement du cadre de navigation. </p> <p>S’il est défini sur <span class="codeph"> onimage </span> , le cadre de navigation ne peut être positionné que dans la zone d’image réelle du  principal. </p> <p>Si cette option est définie pour <span class="codeph"> libérer </span> un utilisateur, celui-ci peut déplacer le cadre de navigation n’importe où dans la zone de  principale logique, même en dehors du contenu de l’image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
