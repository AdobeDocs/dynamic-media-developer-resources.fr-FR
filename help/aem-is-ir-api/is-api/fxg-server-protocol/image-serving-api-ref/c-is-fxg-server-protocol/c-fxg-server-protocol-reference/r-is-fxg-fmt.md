---
description: Format d’image de réponse.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# fmt{#fmt}

Format d’image de réponse.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Indique le format de codage de l’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP. </p> <p> <span class="codeph"> jpeg </span> : JPEG avec perte </p> <p> <span class="codeph"> png </span> : PNG sans perte </p> <p> <span class="codeph"> png-alpha </span> : PNG sans perte avec canal alpha </p> <p> <span class="codeph"></span>tif : TIFF </p> <p> <span class="codeph"> tif-alpha </span>: TIFF avec couche alpha </p> <p> <span class="codeph">  swf </span>: JPEG avec perte incorporé dans un fichier SWF Adobe </p> <p> <span class="codeph"> pdf </span>: image incorporée au format PDF </p> <p> <span class="codeph"> gif </span> : GIF de 2 à 256 couleurs </p> <p> <span class="codeph"> gif-alpha </span> : GIF de 2 à 255 couleurs avec transparence des couleurs clés </p> <p> <span class="codeph"> fxg </span>: FXG avec variables et manipulation DOM appliquées </p> <p> <span class="codeph">  fxgraw </span>: FXG d’origine stocké sur le serveur </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Type de</span> pixel </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> RVB | gris | Cmjn</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Peut être utilisé pour affecter l’espace colorimétrique de sortie. </p> <p> <span class="codeph"> rvb </span> : renvoi des données d’image RGB </p> <p> <span class="codeph"> des </span> gris : renvoi des données d’image en niveaux de gris </p> <p> <span class="codeph"> les </span> CMJN : renvoi des données d’image CMJN </p> </td> 
 </tr> 
</table>

`tiffCompression` n’est autorisé que si tif, tif-alpha est spécifié comme format. Consultez le tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

`qlt=` peut être utilisée pour définir les options d’encodage JPEG pour les formats suivants : JPEG, TIFF avec compression JPEG. quantize= peut être utilisé si fmt=gif ou fmt=gif-alpha. Reportez-vous à la description des commandes pour plus d’informations. Les autres formats ne comportent pas d’options définissables.

8 bits par composant de pixel sont renvoyés pour tous les formats et `pixelTypes[7]`.

Le tableau suivant répertorie les combinaisons valides de format et de `pixelType`, les types MIME de réponse HTTP correspondants.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Type MIME de réponse </p> </th> 
   <th colname="col4" class="entry"> <p>Intégrer le profil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Options </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rvb, gris, cmjn </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>RVB, gris </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rvb, gris, cmjn </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><span class="codeph"><span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>SWF, SWF-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p>&lt;application/x-chokwave-flash&gt; </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>RVB, Gris, CMJN </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>RVB, gris </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
