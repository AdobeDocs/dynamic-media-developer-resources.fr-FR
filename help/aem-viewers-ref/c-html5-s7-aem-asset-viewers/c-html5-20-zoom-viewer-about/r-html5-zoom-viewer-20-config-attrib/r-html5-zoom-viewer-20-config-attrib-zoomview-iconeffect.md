---
description: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
feature: Dynamic Media Classic,Visionneuses,SDK/API,Zoom
role: Developer,User
exl-id: 59d71d3b-706f-4f77-8e75-e24c5654f6e3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Permet à l’effet d’icône <span class="codeph"></span> de s’afficher en haut de l’image lorsque celle-ci est à l’état réinitialisé et qu’il suggère une action disponible pour interagir avec l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois que l’icône <span class="codeph"> </span> apparaît et réapparaît. Une valeur <span class="codeph"> -1</span> indique que l’icône réapparaît toujours indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée de l’animation d’affichage ou de masquage, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>Définit le nombre de secondes pendant lesquelles <span class="codeph"> iconEffet</span> reste entièrement visible avant qu’il ne se masque automatiquement. C’est-à-dire le temps qui suit la fin de l’animation de fondu avant le début de l’animation de fondu. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

`1,1,0.3,3`

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
