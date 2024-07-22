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

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *`duration`*[, *`spacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>Indique le type d’effet appliqué au changement d’image. L’attribut <span class="codeph"> none </span> signifie aucune transition ; le changement d’image se produit instantanément. L’attribut <span class="codeph"> fondu </span> signifie une transition entre les anciennes et les nouvelles images. L’attribut <span class="codeph"> de la diapositive </span> active la transition où l’ancienne image s’éloigne de la vue et la nouvelle image s’y glisse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> duration </span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée (en secondes) de l’effet de transition <span class="codeph"> fondu </span> ou <span class="codeph"> diapositive </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espacement </span> </span> </p> </td> 
   <td colname="col2"> <p>L’espacement entre les images adjacentes dans la transition <span class="codeph"> de la diapositive </span>, est compris entre <span class="codeph"> 0 </span> et <span class="codeph"> 1 </span> et est relatif à la largeur du composant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
