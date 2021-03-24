---
description: Format d’image de réponse.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 3%

---


# fmt{#fmt}

Format d’image de réponse.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Indique le format de codage d’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP. </p> <p> <span class="codeph">  jpeg  </span>: JPEG avec perte </p> <p> <span class="codeph"> png  </span>: PNG sans perte </p> <p> <span class="codeph"> png-alpha  </span>: PNG sans perte avec canal alpha </p> <p> <span class="codeph">  tif  </span>: TIFF </p> <p> <span class="codeph"> tif-alpha  </span>: TIFF avec canal alpha </p> <p> <span class="codeph">  swf  </span>: JPEG avec perte incorporé dans un fichier swf Adobe </p> <p> <span class="codeph"> pdf  </span>: image incorporée dans le PDF </p> <p> <span class="codeph"> gif  </span>: GIF de 2 à 256 couleurs </p> <p> <span class="codeph"> gif-alpha  </span>: GIF de 2 à 255 couleurs + transparence de couleur clé </p> <p> <span class="codeph"> fxg  </span>: FXG avec variables et manipulation DOM appliquées </p> <p> <span class="codeph">  fxgraw  </span>: FXG original stocké sur le serveur </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | gris | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Peut être utilisé pour appliquer l’espace colorimétrique de sortie. </p> <p> <span class="codeph">  rgb  </span>: renvoyer les données d’image RVB </p> <p> <span class="codeph"> gris  </span>: renvoyer des données d’image en niveaux de gris </p> <p> <span class="codeph"> cmyk  </span>: renvoyer les données image CMJN </p> </td> 
 </tr> 
</table>

`tiffCompression` n’est autorisée que si tif, tif-alpha est spécifié comme format. Reportez-vous au tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

`qlt=` peut être utilisé pour définir les options de codage JPEG pour ces formats : JPEG, TIFF avec compression JPEG. quantize= peut être utilisé si fmt=gif ou fmt=gif-alpha. Consultez les descriptions des commandes pour plus de détails. Les autres formats n’ont pas d’options configurables.

Un composant de 8 bits par pixel est renvoyé pour tous les formats et `pixelTypes[7]`.

Le tableau suivant liste les combinaisons valides de format et `pixelType`, les types MIME de réponse HTTP correspondants.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> formater</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Type MIME de réponse </p> </th> 
   <th colname="col4" class="entry"> <p>Incorporer le profil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Options </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, gray, cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p><span class="codeph"> quantifier=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
