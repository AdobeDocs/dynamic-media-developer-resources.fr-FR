---
description: CarouselView.frametransition
solution: Experience Manager
title: CarouselView.frametransition
feature: Dynamic Media Classic,Visionneuses,SDK/API,Bannières de carrousel
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 5%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *``*[, *`durée, espacement`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>Indique le type d’effet appliqué au changement d’image. <span class="codeph"> aucun ne  </span> représente aucune transition; le changement d’image se produit instantanément. </p> <p> <span class="codeph"> fade  </span> signifie transition entre les anciennes et les nouvelles images. </p> <p> <span class="codeph"> La diapositive  </span> active la transition où l’ancien cadre dérive de l’affichage et où le nouveau cadre glisse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée  </span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée (en secondes) de l’effet de transition <span class="codeph"> fondu </span> ou <span class="codeph"> diapositive </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espacement  </span> </span> </p> </td> 
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
