---
title: ZoomView.iconeffect
description: ZoomView.iconeffect
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: faec00b3-b981-4831-bc97-dff442389133
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# ZoomView.iconeffect{#zoomview-iconeffect}

` [ZoomView.|<containerId>_zoomView.]iconeffect=0|1[, *`Count`*][, *`Fade`*][, *`Masquer automatiquement`*]`

<table id="table_6CAA904E976A41BD994D8926F46F0BAF"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Permet à l’effet IconEffect de s’afficher en haut de l’image lorsque l’image est dans un état de réinitialisation et qu’il suggère une action disponible pour interagir avec l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> compter</span> </span> </p> </td> 
   <td colname="col2"> <p> Spécifie le nombre maximal de fois où l’effet IconEffect apparaît et réapparaît. La valeur <span class="codeph"> -1</span> indique que l’icône réapparaît toujours indéfiniment. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> se faner</span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée de l’animation d’affichage ou de masquage, en secondes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> Masquer</span> automatiquement </span> </p> </td> 
   <td colname="col2"> <p>Définit le nombre de secondes pendant lesquelles l’effet IconEffect reste entièrement visible avant d’être masqué automatiquement. C’est-à-dire le temps après la fin de l’animation en fondu mais avant le début de l’animation en fondu. Un paramètre de <span class="codeph"> 0</span> désactive le comportement de masquage automatique. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`1,1,0.3,3`

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

`iconeffect=0`
