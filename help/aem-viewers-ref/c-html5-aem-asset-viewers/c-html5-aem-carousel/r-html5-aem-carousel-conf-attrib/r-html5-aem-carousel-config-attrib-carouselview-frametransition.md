---
title: CarouselView.frametransition
description: CarouselView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 771395fb-775d-462e-86dc-0600cfecb345
TQID: 'https://experienceleague.adobe.com/65cLC5DOqdGrbVpMMy6gLBNL4F3WRqipNqIlpBIK-GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 4%

---

# CarouselView.frametransition{#carouselview-frametransition}

` [CarouselView.|<containerId>_carouselView.]frametransition=none|fade|slide[, *`durée`*[, *`espacement`*]`

<table id="table_D5992FCFF26046079089652B211BB6C5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> aucun|fondu|</span> de diapositives </p> </td> 
   <td colname="col2"> <p>Spécifie le type de l'effet appliqué au changement d'image. Par exemple, <span class="codeph"> aucun </span> signifie aucune transition ; le changement d’image se produit instantanément. Et, </p> <p> <span class="codeph"> fondu </span> signifie une transition de fondu enchaîné entre les anciennes et les nouvelles images. Enfin, </p> <p> <span class="codeph"> diapositive </span> active la transition lorsque l'ancien cadre sort de la vue et que le nouveau cadre y entre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> durée </span> </span> </p> </td> 
   <td colname="col2"> <p>Indique la durée (en secondes) de <span class="codeph">'effet de transition de </span> de diapositives </span> ou <span class="codeph">. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> espacement </span> </span> </p> </td> 
   <td colname="col2"> <p>L'espacement entre les cadres adjacents dans <span class="codeph"> transition de </span> de glissière est compris entre <span class="codeph"> 0 </span> et <span class="codeph"> 1 </span> et est relatif à la largeur du composant. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-1e637b22e8a44d759d588e47576891e6}

Facultatif.

## Par défaut {#section-71fb773f814649b2885aefee68073641}

Aucune

## Exemple {#section-bce98c31f08a4a0ab262fab7f95ba020}

`frametransition=fade,0.3`
