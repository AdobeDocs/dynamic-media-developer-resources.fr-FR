---
title: ZoomView.frametransition
description: ZoomView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: f57a8a2e-63a1-4a59-9a25-b435d0ac39dc
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 4%

---

# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`Espacement des durées`*[, *` `*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Aucun|fondu|diapositive </span> </p> </td> 
   <td colname="col2"> <p>Spécifie le type d’effet appliqué lors du changement d’image. L’attribut <span class="codeph"> none </span> signifie aucune transition ; le changement de trame se produit instantanément. L’attribut <span class="codeph"> Fade </span> signifie une transition en fondu enchaîné entre l’ancienne et la nouvelle image. La diapositive <span class="codeph"> d’attribut </span> active la transition où l’ancienne image glisse hors de la vue et la nouvelle image glisse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> durée </span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée (en secondes) de l’effet de transition de <span class="codeph"> glissement </span> ou de <span class="codeph"> </span> fondu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> espacement </span> </span> </p> </td> 
   <td colname="col2"> <p>L’espacement entre les images adjacentes dans <span class="codeph"> la transition de diapositive </span> a une plage de <span class="codeph"> 0 </span> à <span class="codeph"> 1 </span> et est relatif à la largeur du composant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
