---
description: Format d’image de réponse. Indique le format de codage d’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 4%

---


# fmt{#fmt}

Format d’image de réponse. Indique le format de codage d’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> formater </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG avec perte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>JPG perdant. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>PNG sans perte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>PNG sans perte avec canal alpha. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>TIFF avec canal alpha. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>JPEG avec perte incorporé dans un fichier swf Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>JPEG avec perte et un masque compressé avec déflation incorporés dans un fichier swf Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>Image incorporée dans le PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>PostScript encapsulé binaire non compressé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF de 256 couleurs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF de 255 couleurs + transparence de couleur clé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType  </span> </p> </td> 
  <td class="stentry"> <p>rvb </p> </td> 
  <td class="stentry"> <p>Renvoyer les données d’image RVB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gris </p> </td> 
  <td class="stentry"> <p>Renvoie des données d’image en niveaux de gris. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>Renvoie les données d’image CMJN. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression  </span> </td> 
  <td class="stentry"> <p>aucun </p> </td> 
  <td class="stentry"> <p>Non compressé. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>Compression LZW (Lempel-Ziv-Welch) (sans perte). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Compression "Deflate" (sans perte). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>Compression JPEG (avec perte). </p> </td> 
 </tr> 
</table>

*`pixelType`* a pour effet la conversion de l’espace colorimétrique de sortie lorsque  `icc=` ce paramètre n’est pas spécifié ; le profil de couleurs par défaut correspondant à  *`pixelType`* est appliqué. Si la gestion des couleurs est désactivée, une conversion naïve est appliquée. *`pixelType`* est ignorée lorsque  `icc=` est spécifiée, ce qui détermine le type de pixel de sortie.

*`compression`* n’est autorisée que si tif, tif-alpha ou PDF est spécifié en tant que  *`format`*. Reportez-vous au tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

`qlt-` définit les options de codage JPEG pour ces formats : JPEG, TIFF avec compression JPEG, PDF avec compression JPEG et fichier SWF. Utilisez `quantize=` si `fmt=gif` ou `fmt=gif-alpha`. Consultez les descriptions des commandes pour plus de détails. Les autres formats n’ont pas d’options configurables.

Un composant de 8 bits par pixel est renvoyé pour tous les formats et types de pixels.

Le tableau suivant liste les combinaisons valides de *`format`* et *`pixelType`*, les types MIME de réponse HTTP correspondants, si les profils ICC peuvent être incorporés (voir [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) et les commandes d&#39;option propres au format qui peuvent être appliquées.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> formater </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType  </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Type MIME de réponse </p> </th> 
   <th colname="col4" class="entry"> <p>Incorporer le Profil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Options </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt=  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rvb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt  </span> </p> <p>( <span class="codeph"> qlt= </span> est ignoré sauf si <span class="varname"> tiffCompression </span> est défini sur 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> <p>(Le Flash Player ignore les profils ICC incorporés.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> attribut::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|zip|jpeg), qlt=  </span> </p> <p> ( <span class="codeph"> qlt= </span> est ignoré sauf si <span class="varname"> tiffCompression </span> est défini sur 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> <p>(Les données sont converties en palette après la conversion en gris ou en rgb.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Indique le format de codage des données d’image de réponse envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.

`png-alpha` renvoie une valeur alpha non associée (c’est-à-dire qu’alpha ne prémultiplie pas les valeurs de pixels), tandis que  `tif-alpha`et  `swf-alpha` renvoie une valeur alpha associée (c’est-à-dire que les valeurs alpha sont pré-multipliées avec les valeurs alpha). Le canal alpha correspond à l’inverse du masque d’arrière-plan de la vignette pour `req=img` et au masque de groupe ou d’objet dans le cas de `req=object`. Pour appliquer alpha lors de l’utilisation d’une requête IR imbriquée, ajoutez `fmt=` avec le format de fichier alpha approprié à la requête IR incorporée et à la requête principale. Aucune donnée alpha n’est renvoyée si un profil ICC CMJN ou Niveaux de gris est spécifié avec `icc=`.

## Propriétés {#section-eb12a82c69d84622bcea153dd84d95b3}

Peut se produire n’importe où dans la demande.

## Par défaut {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* par défaut,  `attribute::Format`et  *`tiffCompression`* par défaut  `attribute::TiffEncoding`. *`pixelType`* par défaut,  `rgb` si  `icc=` n’est pas spécifié, sinon il correspond au type de pixel du profil ICC spécifié.

## Voir aussi {#section-c55efc881fc94c70bff91b870e026a7b}

[attribut ::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ,  [attribut::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50),  [attribut::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e),  [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd), iccEmbed=, pathEmbed=,req=, quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)[](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)[
