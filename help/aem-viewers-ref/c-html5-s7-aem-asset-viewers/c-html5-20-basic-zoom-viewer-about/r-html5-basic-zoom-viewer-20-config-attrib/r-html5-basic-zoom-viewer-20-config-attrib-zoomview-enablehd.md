---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 321ca7e2-e3f9-4b0e-8bde-41d8478e1a0b
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`number`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les appareils pour lesquels <span class="codeph"> devicePixelRatio</span> est supérieur à <span class="codeph"> 1</span>, c’est-à-dire les appareils avec un affichage haute densité comme iPhone4 et les appareils similaires. S’il est actif, le composant limite la taille de la demande d’image IS comme si l’appareil avait uniquement un rapport de pixels de <span class="codeph"> 1</span> et réduisait ainsi la bande passante. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nombre</span> </span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le paramètre de limite, le composant n’active la haute densité en pixels que jusqu’à la limite spécifiée. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> always</span> </p> </td> 
   <td colname="col2"> <p>La densité en pixels de l’écran/de l’appareil est toujours prise en compte.</p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Si la densité de pixels de l’écran = 1, alors l’image demandée est de 1 000 x 1 000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Si la densité de pixels d’écran = 1,5, l’image demandée est de 1 500 x 1 500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Si la densité de pixels d’écran = 2, l’image demandée est de 2 000 x 2 000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> never</span> </p> </td> 
   <td colname="col2"> <p>Il utilise toujours une densité de pixels de 1 et ignore la capacité HD de l’appareil. Par conséquent, l’image demandée est toujours de 1 000 x 1 000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>La densité en pixels d’un appareil est demandée et diffusée uniquement si l’image obtenue est inférieure à la limite spécifiée. </p> <p>Le nombre limite s’applique soit à la largeur, soit à la hauteur. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Si la limite est de 1 600 et que la densité de pixels est de 1,5, l’image de 1 500 x 1 500 est diffusée. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Si la limite est de 1 600 et que la densité en pixels est de 2, l’image de 1 000 x 1 000 est diffusée, car l’image de 2 000 x 2 000 dépasse la limite. </p> </li> 
     </ul> </p> <p> <b>Bonne pratique</b> : le nombre limite doit fonctionner avec le paramètre de l’entreprise pour la taille maximale de l’image. Par conséquent, définissez le nombre limite pour qu’il soit égal au paramètre de taille d’image maximale de l’entreprise. </p> </td> 
  </tr> 
 </tbody> 
</table>
