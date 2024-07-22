---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`duration`*[, *`spacing`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide </span> </p> </td> 
   <td colname="col2"> <p>Indique le type d’effet appliqué au changement d’image. Par exemple, <span class="codeph"> none </span> signifie aucune transition ; le changement d’image se produit instantanément. Et, </p> <p> <span class="codeph"> fondu </span> signifie transition entre les anciennes et les nouvelles images. Enfin, </p> <p> <span class="codeph"> La diapositive </span> active la transition où l’ancienne image s’éloigne de la vue et la nouvelle image s’y glisse. </p> </td> 
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

`frametransition=fade,0.3`
