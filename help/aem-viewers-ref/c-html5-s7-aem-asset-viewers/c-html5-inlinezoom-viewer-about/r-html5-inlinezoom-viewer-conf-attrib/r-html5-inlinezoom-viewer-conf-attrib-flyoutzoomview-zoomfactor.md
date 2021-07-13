---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom intégré
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 2%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Indique l’agrandissement de l’image pour la vue déroulante, par rapport à la vue principale. Doit être une valeur entière ou à virgule flottante <span class="codeph"> 1.0</span> ou supérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Vous pouvez spécifier un facteur secondaire facultatif, accessible en cliquant ou en appuyant sur la vue principale lorsque la mise en surbrillance est principale. Cliquez ou appuyez une seconde fois pour revenir au facteur de zoom Principal. Une valeur <span class="codeph"> -1</span> désactive le facteur de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la manière dont le composant gère les petites images. </p> <p>S’il est défini sur <span class="codeph"> 1</span>, le composant met à niveau l’image principale afin qu’elle s’insère dans la vue principale. En outre, l’image de zoom est mise à niveau de sorte qu’elle remplisse complètement la zone de fenêtre déroulante configurée. </p> <p>Si elle est définie sur <span class="codeph"> 0</span>, les petites images s’affichent à leur résolution d’origine et sont centrées dans la zone d’affichage principale et dans la fenêtre déroulante. Vous pouvez configurer un espace blanc supplémentaire autour de l’image avec une propriété CSS d’arrière-plan ou similaire des classes CSS <span class="codeph"> s7flyoutzoomview</span> et <span class="codeph"> s7flyoutzoom</span> dans la fenêtre d’affichage principale et la fenêtre déroulante, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
