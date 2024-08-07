---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 150968d2-aece-4d2a-b5a8-31b03dae25bb
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Indique l’agrandissement de l’image pour la vue déroulante, par rapport à la vue principale. Doit être une valeur entière ou à virgule flottante <span class="codeph"> 1.0</span> ou supérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Vous pouvez spécifier un facteur secondaire facultatif, accessible en cliquant ou en appuyant sur la vue principale lorsque la mise en surbrillance est active. Cliquez ou appuyez une seconde fois pour revenir au facteur de zoom principal. La valeur <span class="codeph"> -1</span> désactive le facteur de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Indique comment le composant gère les petites images. </p> <p>S’il est défini sur <span class="codeph"> 1</span>, le composant met à niveau l’image principale afin qu’elle s’insère dans la vue principale. En outre, l’image de zoom est mise à niveau de sorte qu’elle remplisse complètement la zone de fenêtre déroulante configurée. </p> <p>Si celle-ci est définie sur <span class="codeph"> 0</span>, les petites images s’affichent à leur résolution d’origine et sont centrées dans la zone d’affichage principale et dans la fenêtre déroulante. Vous pouvez configurer un espace blanc supplémentaire qui s’affiche autour de l’image avec une propriété CSS d’arrière-plan ou similaire de la vue <span class="codeph"> s7flyoutzoomview</span> et des classes CSS <span class="codeph"> s7flyoutzoom</span> dans la fenêtre d’affichage principale et la fenêtre déroulante, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
