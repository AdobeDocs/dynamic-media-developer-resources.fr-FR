---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 5%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`durée`*[, *`espacement`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>Indique le type d’effet appliqué au changement d’image. L’attribut <span class="codeph"> none </span> signifie pas de transition; le changement d’image se produit instantanément. L’attribut <span class="codeph"> fade </span> signifie une transition entre les anciennes et les nouvelles images. L’attribut <span class="codeph"> diapositive </span> active la transition où l’ancien cadre défile de l’affichage et où le nouveau cadre se glisse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée </span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée (en secondes) de <span class="codeph"> fade </span> ou <span class="codeph"> diapositive </span> effet de transition. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espacement </span> </span> </p> </td> 
   <td colname="col2"> <p>Espacement entre les images adjacentes dans <span class="codeph"> diapositive </span> transition, présente la plage de <span class="codeph"> 0 </span> through <span class="codeph"> 1 </span> et est relatif à la largeur du composant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
