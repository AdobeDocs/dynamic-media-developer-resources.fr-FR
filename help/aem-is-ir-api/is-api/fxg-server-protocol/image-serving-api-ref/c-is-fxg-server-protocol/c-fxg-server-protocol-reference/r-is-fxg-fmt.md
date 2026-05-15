---
description: Format d’image de réponse.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
TQID: 'https://experienceleague.adobe.com/tqpsn2LTwuUX-SDJTtMKhfpF391ZjjxohgfJn4a-Mdo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 3%

---

# fmt{#fmt}

Format d’image de réponse.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Indique le format de codage de l’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP. </p> <p> </span> jpeg <span class="codeph"> : JPEG avec perte </p> <p> <span class="codeph"> png </span> : PNG sans perte </p> <p> <span class="codeph"> png-alpha </span> : PNG sans perte avec canal alpha </p> <p> <span class="codeph"> tif </span> : TIFF </p> <p> <span class="codeph"> tif-alpha </span> : TIFF avec canal alpha </p> <p> <span class="codeph"> swf </span> : JPEG avec perte incorporée dans un fichier swf Adobe </p> <p> <span class="codeph"> pdf </span> : image incorporée dans PDF </p> <p> <span class="codeph"> gif </span> : GIF de 2 à 256 couleurs </p> <p> <span class="codeph"> gif-alpha </span> : GIF de 2 à 255 couleurs avec transparence des couleurs clés </p> <p> <span class="codeph"> fxg </span> : FXG avec des variables et manipulation DOM appliquée </p> <p> <span class="codeph"> fxgraw </span> : fichier FXG d’origine stocké sur le serveur </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rvb | gris | cmjn</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Peut être utilisé pour appliquer l’espace colorimétrique de sortie. </p> <p> <span class="codeph"> rvb </span> : renvoi des données d’image RGB </p> <p> <span class="codeph"> des </span> gris : renvoi des données d’image en niveaux de gris </p> <p> <span class="codeph"> les </span> CMJN : renvoi des données d’image CMJN </p> </td> 
 </tr> 
</table>

`tiffCompression` n’est autorisé que si tif, tif-alpha est spécifié comme format. Consultez le tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

`qlt=` peut être utilisé pour définir les options de codage JPEG pour les formats suivants : JPEG, TIFF avec compression JPEG. quantize= peut être utilisé si fmt=gif ou fmt=gif-alpha. Reportez-vous à la description des commandes pour plus d’informations. Les autres formats ne comportent pas d’options définissables.

8 bits par composant de pixel sont renvoyés pour tous les formats et `pixelTypes[7]`.

Le tableau suivant répertorie les combinaisons valides de format et de `pixelType`, les types MIME de réponse HTTP correspondants.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Type MIME de réponse </p> </th> 
   <th colname="col4" class="entry"> <p>Incorporer le profil ICC </p> </th> 
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
   <td> <p>rvb, gris </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rvb, gris, cmjn </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p>&lt;application/x-chokwave-flash&gt; </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rvb, gris, cmjn </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>oui </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rvb, gris </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>non </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
