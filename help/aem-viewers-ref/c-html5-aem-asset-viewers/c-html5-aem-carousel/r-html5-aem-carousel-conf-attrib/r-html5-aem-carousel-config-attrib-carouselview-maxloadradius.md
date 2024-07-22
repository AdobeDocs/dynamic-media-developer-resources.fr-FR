---
title: CarouselView.maxloadradius
description: CarouselView.maxloadradius
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 8a3d3d32-7970-420c-8ad8-296c9ba1f08a
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 4%

---

# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Indique le comportement de préchargement du composant. </p> <p>Lorsqu’il est défini sur <span class="codeph"> -1</span>, le composant précharge toutes les images de carrousel en cas d’inactivité. </p> <p>Lorsqu’il est défini sur <span class="codeph"> 0</span>, le composant charge uniquement l’image actuellement visible, précédente et suivante. </p> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> définit le nombre d’images invisibles autour de l’image actuellement affichée qui sont préchargées en cas d’inactivité. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
