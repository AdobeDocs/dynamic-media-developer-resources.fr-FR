---
description: CarouselView.enableHD
solution: Experience Manager
title: CarouselView.enableHD
feature: Dynamic Media Classic,Visionneuses,SDK/API,Bannières de carrousel
role: Developer,User
exl-id: c94ac151-3115-42ac-8a76-13b8769293cb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 6%

---

# CarouselView.enableHD{#carouselview-enablehd}

` [CarouselView.|<containerId>_carouselView.]enableHD=always|never|limit[, *`nombre`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les appareils pour lesquels la valeur <span class="codeph"> devicePixelRatio</span> est supérieure à <span class="codeph"> 1</span>, c’est-à-dire les appareils avec un affichage haute densité comme l’iPhone4 et les appareils similaires. </p> <p>Si principal, le composant limite la taille de la demande d’image IS comme si le périphérique n’avait qu’un rapport de pixels de <span class="codeph"> 1</span> et réduisait ainsi la bande passante. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le paramètre <span class="codeph"> limit</span> , le composant n’active la haute densité en pixels que jusqu’à la limite spécifiée. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`limit,1500`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`enableHD=always`
