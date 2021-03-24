---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
feature: Dynamic Media Classic, Visionneuses, SDK/API, Zoom intégré
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaireFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Indique le facteur de zoom de l’image pour la vue de la fenêtre déroulante, par rapport à la vue principale. Doit être un entier ou une valeur à virgule flottante <span class="codeph"> 1.0</span> ou supérieure. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaireFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Un facteur secondaire facultatif peut être spécifié, accessible en cliquant ou en appuyant sur la vue principale lorsque la mise en surbrillance est principale. Le fait de cliquer ou d’appuyer une seconde fois revient au facteur de zoom Principal. La valeur <span class="codeph"> -1</span> désactive le facteur de zoom secondaire. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> haut</span></span> </p> </td> 
   <td colname="col2"> <p>Indique comment le composant gère les petites images. </p> <p>Si ce paramètre est défini sur <span class="codeph"> 1</span>, le composant met à niveau l’image principale afin qu’elle s’adapte à la vue principale. Il met également à l’échelle l’image de zoom de sorte qu’elle remplisse complètement la zone de fenêtre déroulante configurée. </p> <p>Si elle est définie sur <span class="codeph"> 0</span>, les petites images s’affichent à leur résolution d’origine et s’affichent au centre de la zone de vue principale et à l’intérieur de la fenêtre déroulante. Vous pouvez configurer un espace blanc supplémentaire autour de l’image avec une propriété CSS d’arrière-plan ou similaire des classes CSS <span class="codeph"> s7flyoutzoomview</span> et <span class="codeph"> s7flyoutzoom</span> dans la vue principale et la fenêtre déroulante, respectivement. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-e6310c8c4e8547689a5b48ceddb3671d}

Facultatif.

## Par défaut {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Exemple {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
