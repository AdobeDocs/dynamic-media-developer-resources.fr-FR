---
description: ZoomView.frametransition
solution: Experience Manager
title: ZoomView.frametransition
topic: Dynamic media
uuid: 28e283ca-51d8-4d6c-9b8a-d16da21f4da1
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 5%

---


# ZoomView.frametransition{#zoomview-frametransition}

` [ZoomView.|<containerId>_zoomView.]frametransition=none|fade|slide[, *``*[, *`durationespacement`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|fade|slide  </span> </p> </td> 
   <td colname="col2"> <p>Indique le type de l’effet appliqué au changement d’image. <span class="codeph"> aucun  </span> signifie qu'il n'y a pas de transition ; le changement d'image se produit instantanément. <span class="codeph"> fade  </span> signifie une transition de fondu enchaîné entre les anciennes et les nouvelles images. <span class="codeph"> La diapositive  </span> active la transition dans laquelle l’ancienne image se retire de la vue et la nouvelle image s’y glisse. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée  </span> </span> </p> </td> 
   <td colname="col2"> <p>Spécifie la durée (en seconde) de l'effet de transition <span class="codeph"> fondu </span> ou <span class="codeph"> diapositive </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espacement  </span> </span> </p> </td> 
   <td colname="col2"> <p>L'espacement entre les trames adjacentes dans la transition de la diapositive </span> a la plage comprise entre <span class="codeph"> 0 </span> et <span class="codeph"> 1 </span> et est relatif à la largeur du composant.<span class="codeph"> </span></p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,1`
