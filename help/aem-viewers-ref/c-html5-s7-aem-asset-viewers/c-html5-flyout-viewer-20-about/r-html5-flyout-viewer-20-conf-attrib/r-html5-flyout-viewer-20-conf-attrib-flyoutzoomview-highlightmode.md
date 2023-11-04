---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> highlight|cursor </span> </p> </td> 
   <td colname="col2"> <p> Indique le type de cadre de navigation à utiliser. Lorsque la variable est définie sur <span class="codeph"> cursor </span>, le composant utilise un curseur de référence à taille fixe. Il est possible d’avoir différentes formes de curseur pour les ordinateurs de bureau et les appareils tactiles. Cette fonctionnalité est contrôlée par <span class="codeph"> .s7cursor </span> Classe CSS et <span class="codeph"> input=mouse|touch </span> sélecteur d’attributs. Sur les ordinateurs de bureau, un point d’ancrage est défini au milieu de la zone du curseur, tandis que sur les périphériques tactiles, il se trouve au centre inférieur du curseur. Lorsque la variable est définie sur <span class="codeph"> highlight </span>, le composant utilise un cadre de navigation de taille variable ; la taille et la forme du cadre dépendent du facteur de zoom et de la taille de la vue déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Définit le temps (en secondes) nécessaire à la mise en surbrillance ou au fondu du curseur après son activation par l’utilisateur. L’option Fondu n’est appliquée que sur les appareils tactiles ; sur les ordinateurs de bureau, elle est ignorée par le composant. </p> <p>Le fondu s’applique aux éléments de l’interface utilisateur suivants : cadre de surbrillance, curseur fixe, superposition (au cas où <span class="codeph"> superposition </span> est défini sur <span class="codeph"> 1 </span>). L’animation de la vue déroulante ne commence qu’une fois le surlignage/le fondu du curseur terminé dans l’animation. Il n'y a pas d'animation en fondu. Lorsque l’utilisateur désactive la fenêtre déroulante, les éléments d’IU correspondants (curseur, surbrillance et recouvrement) se masquent instantanément. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|free </span> </p> </td> 
   <td colname="col2"> <p> Contrôle le positionnement du cadre de navigation. </p> <p>Si la variable est définie sur <span class="codeph"> onimage </span>, le cadre de navigation ne peut être positionné que dans la zone de l’image dans la vue principale. </p> <p>Si la variable est définie sur <span class="codeph"> free </span> un utilisateur peut déplacer le cadre de navigation n’importe où dans la zone d’affichage principale logique, même en dehors du contenu de l’image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
