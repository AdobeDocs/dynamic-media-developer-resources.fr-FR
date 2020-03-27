---
description: Paramètre commun à toutes les visionneuses.
seo-description: Paramètre commun à toutes les visionneuses.
seo-title: asset
solution: Experience Manager
title: asset
topic: Dynamic media
uuid: 6a72257f-d204-4258-b6f8-de6f7b00fd54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# asset{#asset}

Paramètre commun à toutes les visionneuses.

` asset= *`assetId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetId </span></span> </p> </td> 
   <td colname="col2"> <p> ID de fichier de la vidéo unique ou de la visionneuse de vidéos adaptative. </p> </td> 
  </tr> 
 </tbody> 
</table>

Cette propriété est requise, sauf si `video` un paramètre est utilisé. Reportez-vous à la page Prise en charge [vidéo](../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3) externe sous Vidéo ou Prise en charge [vidéo](../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-external-video-support.md#concept-66aa2784f2294794989bad2af74c3760) externe sous Vidéo360.

ou

` asset= *`image`*`

<table id="table_67E18F42E97C4AAAB0A2F67B7924765D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image </span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie une image unique ou un jeu de carrousel. Appliquez  codage HTTP à tout caractère non sécurisé figurant dans le nom de l’image ou le nom du jeu de carrousel. </p> </td> 
  </tr> 
 </tbody> 
</table>

ou

` asset= *``* | *``* | *``* | *``* [%3F *`imageimageListimageListWithModifiersmultiDimensionalSpinSetmodiers`*]`

<table id="table_A2A0ACD942E942BC99AF0DC80FB1C670"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image </span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie une image unique. Appliquez  codage HTTP à tout caractère non sécurisé figurant dans le nom de l’image. </p> <p>Vous pouvez également spécifier une référence à une visionneuse d’images. Le lecteur récupère les visionneuses d’images à partir du serveur, à l’aide de la <span class="codeph"> </span> requête IS req=set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageList </span></span> </p> </td> 
   <td colname="col2"> <p> Indique une visionneuse d’images explicite, composée d’une séquence triée d’éléments ou de cadres, séparés par des virgules. </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> imageListWithModifiers </span></span> </p> </td> 
   <td colname="col2"> <p> Indique une visionneuse d’images explicite dans laquelle chaque image possède ses propres modificateurs de diffusion d’images. Dans ce cas, le de cadres est placé entre parenthèses. Veillez à appliquer le codage HTTP  à toute virgule présente dans le modificateur Image Serving spécifique aux images. </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> multi-DimensionalSpinSet </span></span> </p> </td> 
   <td colname="col2"> <p>Spécifie une visionneuse à 360° multidimensionnelle explicite à l’aide de la syntaxe suivante : </p> <p> <span class="codeph"> (( <span class="varname"> horizontalSpinSet </span>)[,( <span class="varname"> horizontalSpinSet </span>)]) </span> </p> <p> où <span class="codeph"> la visionneuse à 360° <span class="varname"> horizontale </span> </span> est un d’images séparé par des virgules pour un axe horizontal donné. Toutes les visionneuses à 360° <span class="codeph"> <span class="varname"> horizontales </span> </span> doivent avoir le même nombre d’images. </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificateurs </span></span> </p> </td> 
   <td colname="col2"> <p> Image Serving, commandes ; Les séparateurs <span class="codeph"> &amp; </span> et <span class="codeph"> = </span> doivent être codés en HTTP comme <span class="codeph"> %26 </span> et <span class="codeph"> %3D , respectivement.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

ou

` asset=( *``* | ( *``*; *``* | *``*; *``* | *``*; *``*); *``*;( *``*; *``* | *``*; *``* | *``*; *``*); *``*;] [%3F *`mediaSetvideoswatchIdimageswatchIdsetIdswatchIdvideoswatchIdimageswatchIdsetIdswatchIdIDmodiers`*]`

<table id="table_D31C8507C02A4452A79DEDDEC62EF2F5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> mediaSet </span></span> </p> </td> 
   <td colname="col2"> <p> Spécifie une référence à une visionneuse de supports. Le lecteur récupère les visionneuses de supports à partir du serveur, à l’aide de la requête IS req=set. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> vidéo </span></span> </p> </td> 
   <td colname="col2"> <p> Vidéo unique ou visionneuse de vidéos adaptative. </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> image </span></span> </p> </td> 
   <td colname="col2"> <p> Image unique. </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> setId </span></span> </p> </td> 
   <td colname="col2"> <p> Série d’échantillons. </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> swatchId </span></span> </p> </td> 
   <td colname="col2"> <p>Image d’échantillon. </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID </span></span> </p> </td> 
   <td colname="col2"> <p> L’identifiant de type d’élément de la visionneuse de supports peut être l’un des suivants : </p> <p> 
     <ul id="ul_3100F9356628498DA820C07F6F69CC9B"> 
      <li id="li_51B649A539F14510873CFDA85A6AA714"> <p> <span class="codeph"> advanced_image </span> </p> <p>Pour une image unique. </p> </li> 
      <li id="li_7E764D67294647C1A828F949E5ED1908"> <p> <span class="codeph"> advanced_swatchset </span> </p> <p>Pour la visionneuse d’échantillons imbriquée. </p> </li> 
      <li id="li_C942CED779B54110BCDC74188995FD5B"> <p> <span class="codeph"> spin </span> </p> <p>Pour la visionneuse à 360°. </p> </li> 
      <li id="li_6EA5C54F078D4B24B44F1588BF083842"> <p> <span class="codeph"> video </span> </p> <p>Pour une vidéo unique. </p> </li> 
      <li id="li_8110FA7E0CAB4681A2D8C15F2A656E69"> <p> <span class="codeph"> video_set </span> </p> <p>Pour Les Visionneuses De Vidéos Adaptatives. </p> </li> 
     </ul> </p> <p> <p>Remarque :  Cette fonctionnalité est prise en charge dans Adobe Scene7 Publishing System ; il n’est pas pris en charge dans les ressources d’Adobe Experience Manager. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> modificateurs </span></span> </p> </td> 
   <td colname="col2"> <p> Image Serving, commandes ; Les séparateurs <span class="codeph"> &amp; </span> et <span class="codeph"> = </span> doivent être codés en HTTP comme <span class="codeph"> %26 </span> et <span class="codeph"> %3D , respectivement.</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Les images qui utilisent la fonction IR (Image Rendering) ou UGC (User-Generated Content) ne sont pas prises en charge par cette visionneuse.

## Propriétés {#section-10ee45d637134e0fbcd943c62578cb78}

Obligatoire.

## Par défaut {#section-d411e450028c460392cb8508f8ccc5d9}

Aucune

## Exemples {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

Référence d’élément unique :

```
asset=Scene7SharedAssets/Backpack_B
```

ou

```
asset=/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg
```

ou

```
asset=/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4
```

ou

```
asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner
```

ou

```
asset=Viewers/space_station_360-AVS
```

Référence unique à une visionneuse d’images définie dans un catalogue :

```
asset=Viewers/Pluralist
```

Visionneuse d’images explicite :

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C
```

Visionneuse d’images explicite avec modificateurs de diffusion d’images spécifiques aux images :

```
asset=(Scene7SharedAssets/Backpack_B%3Fop_colorize%3D255%252C0%252C0,Scene7SharedAssets/Backpack_B%3Fop_colorize%3D0x00ff00)
```

Référence unique à une visionneuse à 360° définie dans un catalogue :

```
asset=Scene7SharedAssets/SpinSet-Sample
```

Visionneuse à 360° explicite :

```
asset=Scene7SharedAssets/Frame-1,Scene7SharedAssets/Frame-2,Scene7SharedAssets/Frame-3,Scene7SharedAssets/Frame-4,Scene7SharedAssets/Frame-5,Scene7SharedAssets/Frame-6,Scene7SharedAssets/Frame-7,Scene7SharedAssets/Frame-8
```

Visionneuse à 360° multidimensionnelle explicite :

```
asset=((Scene7SharedAssets/ring1-25,Scene7SharedAssets/ring1-26,Scene7SharedAssets/ring1-27,Scene7SharedAssets/ring1-28,Scene7SharedAssets/ring1-29,Scene7SharedAssets/ring1-30,Scene7SharedAssets/ring1-31,Scene7SharedAssets/ring1-32,Scene7SharedAssets/ring1-33,Scene7SharedAssets/ring1-34,Scene7SharedAssets/ring1-35,Scene7SharedAssets/ring1-36),(Scene7SharedAssets/ring1-13,Scene7SharedAssets/ring1-14,Scene7SharedAssets/ring1-15,Scene7SharedAssets/ring1-16,Scene7SharedAssets/ring1-17,Scene7SharedAssets/ring1-18,Scene7SharedAssets/ring1-19,Scene7SharedAssets/ring1-20,Scene7SharedAssets/ring1-21,Scene7SharedAssets/ring1-22,Scene7SharedAssets/ring1-23,Scene7SharedAssets/ring1-24),(Scene7SharedAssets/ring1-01,Scene7SharedAssets/ring1-02,Scene7SharedAssets/ring1-03,Scene7SharedAssets/ring1-04,Scene7SharedAssets/ring1-05,Scene7SharedAssets/ring1-06,Scene7SharedAssets/ring1-07,Scene7SharedAssets/ring1-08,Scene7SharedAssets/ring1-09,Scene7SharedAssets/ring1-10,Scene7SharedAssets/ring1-11,Scene7SharedAssets/ring1-12))
```

Référence de jeu de supports mixtes unique :

```
 asset=Scene7SharedAssets/Mixed_Media_Set_Sample
```

Visionneuse de supports variés explicites :

```
asset=Scene7SharedAssets/Backpack_J;;advanced_image;,Scene7SharedAssets/Frame-6;;advanced_image;,Scene7SharedAssets/Frame-2;;advanced_image;,Scene7SharedAssets/SpinSet_Sample;;spin;,Scene7SharedAssets/ImageSet-Colors-Sample;;advanced_swatchset;,Scene7SharedAssets/Glacier_Climber_640x360;Scene7SharedAssets/Glacier_Climber_640x360;video;
```

Modificateur d’accentuation ajouté à toutes les images de la visionneuse :

```
asset=Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C%3Fop_sharpen=%3D1
```

```
asset=Scene7SharedAssets/Mixed_Media_Set_Sample%3Fop_sharpen%3D1
```

```
asset=Viewers/Pluralist%3Fop_sharpen%3D1
```

