---
title: FlyoutZoomView.highlightmode
description: FlyoutZoomView.highlightmode
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: b35285a2-7319-4ed7-9681-12a6acda8fa5
TQID: 'https://experienceleague.adobe.com/x43ipzx6iKOODZ10S8o8yJA9pg0Gl8mldfS5fEiVQJ4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 258
ht-degree: 1%

---

# FlyoutZoomView.highlightmode{#flyoutzoomview-highlightmode}

` [FlyoutZoomView.|<containerId>_flyout.]highlightmode=highlight|cursor[, *`showtime`*[,onimage|free]]`

<table id="table_C6F4C663099F40698874731590A22924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> en surbrillance|</span> du curseur </p> </td> 
   <td colname="col2"> <p> Spécifie le type de cadre de navigation à utiliser. Lorsqu’il est défini sur <span class="codeph"> curseur </span>, le composant utilise un curseur de référence de taille fixe. Il est possible d’avoir des dessins de curseur différents pour les ordinateurs de bureau et les appareils tactiles. Cette fonctionnalité est contrôlée avec <span class="codeph"> classe CSS .s7cursor </span> et <span class="codeph"> sélecteur d’attributs input=ouse|touch </span>. Sur les ordinateurs de bureau, un point d’ancrage est défini au milieu de la zone du curseur, tandis que sur les appareils tactiles, l’ancrage se trouve au centre inférieur du curseur. Lorsqu’il est défini sur <span class="codeph"> mise en surbrillance </span>, le composant utilise un cadre de navigation de taille variable ; la taille et la forme du cadre dépendent du facteur de zoom et de la taille de la vue déroulante. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> showtime </span> </span> </p> </td> 
   <td colname="col2"> <p> Définit le temps (en secondes) nécessaire pour que la mise en surbrillance ou le curseur s’estompe après son activation par l’utilisateur. Le fondu entrant est appliqué uniquement sur les appareils tactiles ; sur les ordinateurs de bureau, il est ignoré par le composant. </p> <p>Le fondu dans s’applique aux éléments suivants de l’interface utilisateur : cadre de surbrillance, curseur fixe, recouvrement (si <span class="codeph"> paramètre de </span> de recouvrement est défini sur <span class="codeph"> 1 </span>). L’animation en mode Fenêtre déroulante ne commence qu’après le fondu de la surbrillance/du curseur dans l’animation. Il n'y a pas d'animation en fondu. Lorsque l’utilisateur désactive la fenêtre déroulante, les éléments d’IU correspondants (curseur, mise en surbrillance et recouvrement) sont instantanément masqués. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> onimage|</span> gratuit </p> </td> 
   <td colname="col2"> <p> Contrôle le positionnement du cadre de navigation. </p> <p>S’il est défini sur <span class="codeph"> sur les </span> d’image, le cadre de navigation ne peut être positionné qu’à l’intérieur de la zone d’image réelle dans la vue principale. </p> <p>S’il est défini sur <span class="codeph"> libre </span>’un utilisateur peut déplacer le cadre de navigation n’importe où dans la zone d’affichage principale logique, même en dehors du contenu de l’image. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`highlight,0.1,onimage`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`highlightmode=cursor,1,free`
