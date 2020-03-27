---
description: 'null'
seo-description: 'null'
seo-title: ZoomView.enableHD
solution: Experience Manager
title: ZoomView.enableHD
topic: Dynamic media
uuid: 1ee3789d-a3eb-42f7-a0f4-71f62a54cab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`nombre`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|jamais|limit</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les périphériques pour lesquels le <span class="codeph"> rapportPixelRatio</span> est supérieur à <span class="codeph"> 1</span>, c’est-à-dire les périphériques avec un affichage haute densité comme l’iPhone4 et les périphériques similaires. S’il est actif, le composant limite la taille de la demande d’image IS comme si le périphérique n’avait qu’un rapport de pixels de <span class="codeph"> 1</span> et réduisait ainsi la bande passante. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> numéro</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le paramètre de limite, le composant n’active la haute densité de pixels que jusqu’à la limite spécifiée. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-50bcd15223174bb79ce08b31ea03d682}

Facultatif.

## Par défaut {#section-7564169749ff4a4996049ea1148cb2a5}

`limit,1500`

## Exemple {#section-96e69b70365f461dae4399e49044ea2f}

Voici les résultats attendus lorsque vous utilisez cet attribut de configuration avec la visionneuse et que la taille de la visionneuse est de 1 000 x 1 000 :

<table id="table_F97FEDA0EE1B4EF6AC9FF9060548ACA4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si la variable définie est égale à </p> </th> 
   <th colname="col2" class="entry"> <p>Résultat </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toujours</span> </p> </td> 
   <td colname="col2"> <p>La densité de pixels de l’écran/du périphérique est toujours prise en compte. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Si la densité de pixels de l’écran est égale à 1, l’image demandée est de 1 000 x 1 000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Si la densité de pixels de l’écran est égale à 1,5, l’image demandée est de 1 500 x 1 500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Si la densité de pixels de l’écran est égale à 2, l’image demandée est de 2 000 x 2 000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jamais</span> </p> </td> 
   <td colname="col2"> <p>Il utilise toujours une densité de pixels de 1 et ignore la fonctionnalité HD du périphérique. Par conséquent, l’image demandée est toujours de 1 000 x 1 000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>La densité de pixels d’un périphérique est demandée et diffusée uniquement si l’image obtenue est inférieure à la limite spécifiée. </p> <p>Le nombre limite s’applique soit à la largeur, soit à la hauteur. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Si le nombre maximal est 1600 et que la densité de pixels est 1,5, l’image 1500 x 1500 est diffusée. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Si le nombre limite est de 1 600 et que la densité de pixels est de 2, l’image de 1 000 x 1 000 est diffusée car l’image de 2 000 x 2 000 dépasse la limite. </p> </li> 
     </ul> </p> <p> <b>Meilleure pratique</b>: Le nombre limite doit fonctionner conjointement avec le paramètre de  du pour l’image de taille maximale. Par conséquent, définissez le nombre limite sur le paramètre de taille d’image maximale  par le. </p> </td> 
  </tr> 
 </tbody> 
</table>

