---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor </span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie le zoom de l'image pour la vue déroulante, par rapport à la vue principale. Doit être un entier ou une valeur à virgule flottante <span class="codeph"> 1,0</span> ou supérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Vous pouvez spécifier un facteur secondaire facultatif accessible en cliquant ou en appuyant sur la vue principale lorsque la mise en surbrillance est active. Cliquez ou appuyez une deuxième fois pour rétablir le facteur de zoom principal. Une valeur de <span class="codeph"> -1</span> désactive le facteur de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> haut de gamme</span></span> </p> </td> 
   <td colname="col2"> <p>Indique comment le composant gère les petites images. </p> <p>S’il est défini sur la <span class="codeph"> 1</span> le composant redimensionne l’image principale afin qu’elle s’adapte à la vue principale. En outre, il met à l’échelle l’image du zoom afin qu’elle remplisse complètement la zone de fenêtre déroulante configurée. </p> <p>Si cette valeur est définie sur <span class="codeph"> 0</span>, les petites images s’affichent à leur résolution d’origine et sont centrées dans la zone d’affichage principale et à l’intérieur de la fenêtre déroulante. Vous pouvez configurer un espace blanc supplémentaire autour de l’image avec une propriété CSS d’arrière-plan ou similaire des classes CSS <span class="codeph"> s7flyoutzoomview</span> et <span class="codeph"> s7flyoutzoom</span> dans la vue principale et la fenêtre déroulante, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
