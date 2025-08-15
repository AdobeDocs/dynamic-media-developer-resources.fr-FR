---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: fd81cd48-9990-4659-a52c-7abdbc95a0e3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`number`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toujours|jamais|limite</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les appareils pour lesquels <span class="codeph"> devicePixelRatio</span> est supérieur à <span class="codeph"> 1</span>, c’est-à-dire les appareils dotés d’un affichage à haute densité tels qu’iPhone4 et les appareils similaires. S’il est actif, le composant limite la taille de la demande d’image IS comme si l’appareil avait uniquement un rapport pixel de <span class="codeph"> 1</span> ce qui réduit la bande passante. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> numéro</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le paramètre de limite, le composant n’active une densité de pixels élevée que jusqu’à la limite spécifiée. </p> <p>Voir l’exemple ci-dessous. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-924163cb2f6542499f49894becef7fb5}

Facultatif.

## Par défaut {#section-7a2128fd488941948aff18421f533ccf}

`limit,1500`

## Exemple {#section-622348a84fbe4ff4b5dd7eb53b044d83}

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
   <td colname="col1"> <p><span class="codeph"> toujours</span> </p> </td> 
   <td colname="col2"> <p>La densité en pixels de l’écran/de l’appareil est toujours prise en compte. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Si la densité en pixels de l’écran = 1, l’image demandée est de 1 000 x 1 000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Si la densité en pixels de l’écran = 1,5, l’image demandée est de 1 500 x 1 500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Si la densité en pixels de l’écran = 2, l’image demandée est 2 000 x 2 000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jamais</span> </p> </td> 
   <td colname="col2"> <p>Il utilise toujours une densité de pixels de 1 et ignore la fonctionnalité HD de l’appareil. Par conséquent, l’image demandée est toujours 1 000 x 1 000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limit&lt;number&gt;</span> </p> </td> 
   <td colname="col2"> <p>Une densité en pixels d’appareil est demandée et diffusée uniquement si l’image obtenue est inférieure à la limite spécifiée. </p> <p>Le nombre limite s’applique à la dimension de largeur ou de hauteur. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Si le nombre limite est 1 600 et que la densité de pixels est de 1,5, l’image 1 500 x 1 500 est diffusée. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Si le nombre limite est de 1 600 et que la densité en pixels est de 2, l’image 1 000 x 1 000 est diffusée, car l’image 2 000 x 2 000 dépasse la limite. </p> </li> 
     </ul> </p> <p><b>Bonne pratique </b> : le nombre limite doit fonctionner avec le paramètre d’entreprise pour une image de taille maximale. Par conséquent, définissez le nombre limite pour qu’il soit égal au paramètre de taille d’image maximale de la société. </p> </td> 
  </tr> 
 </tbody> 
</table>
