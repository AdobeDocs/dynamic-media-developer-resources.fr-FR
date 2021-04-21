---
description: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Indique le comportement de préchargement du composant. </p> <p>Lorsqu'il est défini sur <span class="codeph"> -1</span>, le composant précharge toutes les trames du carrousel en cas d'inactivité. </p> <p>Lorsqu'il est défini sur <span class="codeph"> 0</span>, le composant charge uniquement l'image actuellement visible, précédente et suivante. </p> <p><span class="codeph"><span class="varname"> </span></span>preloadnbrdéfinit le nombre de cadres invisibles autour du cadre actuellement affiché qui sont préchargés en cas d’inactivité. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
