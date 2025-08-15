---
title: CarouselView.enableHD
description: CarouselView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`nombre`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toujours|jamais|limite</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les appareils sur lesquels <span class="codeph"> devicePixelRatio</span> est supérieur à <span class="codeph"> 1</span>, c’est-à-dire les appareils dotés d’un écran haute densité comme l’iPhone4 et les appareils similaires. </p> <p>S’il est actif, le composant limite la taille de la demande d’image IS comme si le périphérique n’avait qu’un rapport de pixels de <span class="codeph"> 1</span> , réduisant ainsi la bande passante. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le <span class="codeph"> paramètre de limite</span> , le composant permet une densité de pixels élevée uniquement jusqu’à la limite spécifiée. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
