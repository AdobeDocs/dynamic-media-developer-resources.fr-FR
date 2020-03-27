---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.iconeffect
solution: Experience Manager
title: ZoomView.iconeffect
topic: Dynamic media
uuid: 38350e3d-515b-454c-bc85-39b91ad06e8b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Permet à IconEffect de s’afficher en haut de l’image lorsque celle-ci est à l’état réinitialisé et suggère une action disponible pour interagir avec l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span></span> </p> </td> 
   <td colname="col2"> <p> Indique le nombre maximal de fois que l’effet IconEffect apparaît et réapparaît. La valeur <span class="codeph"> -1</span> indique que l’icône réapparaît toujours indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>Indique la durée de l’animation d’affichage ou de masquage, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoMasquer</span></span> </p> </td> 
   <td colname="col2"> <p>Définit le nombre de secondes pendant lesquelles IconEffect reste entièrement visible avant d’être masqué automatiquement. C’est-à-dire le moment qui suit la fin de l’animation en fondu mais avant le  d’animation en fondu. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
