---
description: 'null'
seo-description: 'null'
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaireFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> principalFacteur</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le facteur de zoom de l’image pour le  de la fenêtre déroulante, par rapport au principal. Doit être un nombre entier ou une valeur à virgule flottante <span class="codeph"> 1,0</span> ou plus. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaireFactor</span></span> </p> </td> 
   <td colname="col2"> <p> Un facteur secondaire facultatif peut être spécifié, accessible en cliquant ou en appuyant sur le principal lorsque la mise en surbrillance est active. Cliquer ou appuyer une seconde fois revient au facteur de zoom principal. La valeur <span class="codeph"> -1</span> désactive le facteur de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> supérieur</span></span> </p> </td> 
   <td colname="col2"> <p>Indique comment le composant gère les petites images. </p> <p>Si cette valeur est définie sur <span class="codeph"> 1</span> , le composant met à l’échelle l’image principale afin qu’elle s’adapte au  principal du. Il met également à l’échelle l’image de zoom afin qu’elle remplisse complètement la zone de fenêtre déroulante configurée. </p> <p>Si la valeur est définie sur <span class="codeph"> 0</span> petites images, elles s’affichent à leur résolution d’origine et sont centrées dans la zone de  principale et dans la fenêtre déroulante. Vous pouvez configurer un espace blanc supplémentaire qui s’affiche autour de l’image avec une propriété CSS d’arrière-plan ou similaire des classes CSS <span class="codeph"> s7flyoutzoomview</span> et <span class="codeph"> s7flyoutzoom</span> dans la  principale et la fenêtre déroulante, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Facultatif.

## Par défaut {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Exemple {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
