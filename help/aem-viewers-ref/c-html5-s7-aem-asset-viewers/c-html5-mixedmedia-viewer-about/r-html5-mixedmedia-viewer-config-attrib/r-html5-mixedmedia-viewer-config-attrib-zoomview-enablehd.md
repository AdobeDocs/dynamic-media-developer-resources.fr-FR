---
title: ZoomView.enableHD
description: ZoomView.enableHD
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f6b25105-7b70-48f7-b3d6-e53110fd628b
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '308'
ht-degree: 1%

---

# ZoomView.enableHD{#zoomview-enablehd}

` [ZoomView.|<containerId>_zoomView.]enableHD=always|never|limit[, *`nombre`*]`

<table id="table_0BEA0B5FFDF64E5594B534B2A87A6D88"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toujours|jamais|limite</span> </p> </td> 
   <td colname="col2"> <p> Activez, limitez ou désactivez l’optimisation pour les appareils sur lesquels <span class="codeph"> devicePixelRatio</span> est supérieur à <span class="codeph"> 1</span>, c’est-à-dire les appareils dotés d’un écran haute densité comme l’iPhone4 et les appareils similaires. S’il est actif, le composant limite la taille de la demande d’image IS comme si le périphérique n’avait qu’un rapport de pixels de <span class="codeph"> 1</span> , réduisant ainsi la bande passante. </p> <p>Voir l’exemple 2 ci-dessous. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> nombre</span></span> </p> </td> 
   <td colname="col2"> <p> Si vous utilisez le paramètre de limite, le composant permet une densité de pixels élevée uniquement jusqu’à la limite spécifiée. </p> <p>Voir l’exemple 2 ci-dessous. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-65be9301796240e38f31818229da7acc}

Facultatif.

## Par défaut {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Exemple {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Voici les résultats attendus lorsque vous utilisez cet attribut de configuration avec la visionneuse et que la taille de la visionneuse est de 1000 x 1000 :

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
   <td colname="col2"> <p>La densité en pixels de l’écran/périphérique est toujours prise en compte. </p> <p> 
     <ul id="ul_D8F31FDFCDB74B75A3B1BFBEE33AF2E2"> 
      <li id="li_8A1C6DCCE10545349C73029729211BB2"> <p>Si la densité de pixels d’écran = 1, l’image demandée est de 1000 x 1000. </p> </li> 
      <li id="li_884156A34AC64B4E9B3ACC4C25EB710F"> <p>Si la densité de pixels d’écran = 1,5, l’image demandée est de 1500 x 1500. </p> </li> 
      <li id="li_7EC699284A7F4E679E512C3DA8B5454F"> <p>Si la densité de pixels d’écran = 2, l’image demandée est de 2000 x 2000. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> jamais</span> </p> </td> 
   <td colname="col2"> <p>Il utilise toujours une densité de pixels de 1 et ignore la capacité HD de l’appareil. Par conséquent, l’image demandée est toujours égale à 1000 x 1000. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> limite&lt;number&gt;</span>&lt;/number&gt; </p> </td> 
   <td colname="col2"> <p>Une densité de pixels de périphérique est demandée et diffusée uniquement si l’image résultante est inférieure à la limite spécifiée. </p> <p>Le nombre limite s’applique soit à la dimension largeur, soit à la dimension hauteur. </p> <p> 
     <ul id="ul_CEC06B2280164951BA1A0ADED99E8050"> 
      <li id="li_CA7A0980ACC54690A4F212DF53E2DC8A"> <p>Si le nombre limite est de 1600 et que la densité en pixels est de 1,5, l’image 1500 x 1500 est diffusée. </p> </li> 
      <li id="li_A4AAD7FBFA0347B082789511CA6768A5"> <p>Si le nombre limite est de 1600 et que la densité de pixels est 2, l’image 1000 x 1000 est diffusée car l’image 2000 x 2000 dépasse la limite. </p> </li> 
     </ul> </p> <p><b>Bonne pratique</b> : Le nombre limite doit fonctionner avec le paramètre de l’entreprise pour l’image de taille maximale. Par conséquent, définissez le nombre limite pour qu’il soit égal à la taille d’image maximale définie par l’entreprise. </p> </td> 
  </tr> 
 </tbody> 
</table>
