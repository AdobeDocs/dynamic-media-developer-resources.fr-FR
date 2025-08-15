---
title: fmt
description: Format de l’image de réponse. Indique le format de codage de l’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 4%

---

# fmt {#fmt}

Format de l’image de réponse. Indique le format de codage de l’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.

` fmt= *`format`*[,[ *`pixelType`*][, *`tiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> du format </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG avec perte. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>JPG avec perte. </p> </td> 
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
  <td class="stentry"> <p>TIF </p> </td> 
  <td class="stentry"> <p>BROUILLE. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>TIFF avec couche alpha. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>JPEG avec perte incorporé dans un fichier swf Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>JPEG avec perte et masque dégonflé compressé incorporé dans un fichier SWF Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>Image incorporée dans PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>PostScript encapsulée binaire non compressée. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF en 256 couleurs. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF avec 255 couleurs et une transparence des couleurs clés. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
  <td class="stentry"> <p>rvb </p> </td> 
  <td class="stentry"> <p>Renvoie des données d’image RVB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gris </p> </td> 
  <td class="stentry"> <p>Renvoie des données d’image en niveaux de gris. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>Cmjn </p> </td> 
  <td class="stentry"> <p>Renvoie des données d’image CMJN. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> Compression tiff </span> </td> 
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
  <td class="stentry"> <p>Compression « dégonflée » (sans perte). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>Compression JPEG (avec perte). </p> </td> 
 </tr> 
</table>

*`pixelType`* Effets convertissent l’espace colorimétrique de sortie lorsque `icc=` n’est pas spécifié ; le profil colorimétrique par défaut correspondant à *`pixelType`* est appliqué. Si la gestion des couleurs est désactivée, une conversion naïve est appliquée. *`pixelType`* est ignoré lorsque `icc=` est spécifié, ce qui détermine le type de pixel de sortie.

*`compression`* Autorisé uniquement si tif, tif-alpha ou PDF est spécifié comme .*`format`* Reportez-vous au tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

`qlt-` Définit les options de codage JPEG pour les formats suivants : JPEG, TIFF avec compression JPEG, PDF avec compression JPEG et fichier SWF. Utilisez `quantize=` si `fmt=gif` ou `fmt=gif-alpha`. Reportez-vous aux descriptions des commandes pour plus d’informations. Les autres formats ne disposent pas d’options définissables.

Huit bits par composant de pixel sont renvoyés pour tous les formats et types de pixels.

Le tableau suivant répertorie les combinaisons valides de et *`format`*, les types MIME *`pixelType`* de réponse HTTP correspondants, si les profils ICC peuvent être incorporés (voir [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) et quelles commandes d’option spécifiques au format peuvent être appliquées.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> format </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> Type de pixel </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Type MIME de réponse </p> </th> 
   <th colname="col4" class="entry"> <p>Intégrer le profil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Options </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rvb, gris, cmjn </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rvb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rvb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image ng=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>RVB, Gris, CMJN </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image iff=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="varname"> Compression tiff </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt </span> </p> <p><span class="codeph">( qlt= </span> est ignoré sauf si <span class="varname"> tiffCompression </span> est défini sur 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SWF, SWF-alpha </p> </td> 
   <td colname="col2"> <p>RVB, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-chokwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> <p>(Flash Player ignore les profils ICC incorporés.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rvb, gris, cmjn </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> est ignoré sauf si <span class="varname"> tiffCompression </span> est définie sur 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Eps </p> </td> 
   <td colname="col2"> <p>RVB, Gris, CMJN </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image ps=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rvb, gris </p> <p>(Les données sont converties en palette après conversion en gris ou en rvb.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Indique le format de codage des données d’image de réponse envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.

`png-alpha` renvoie la valeur alpha non associée (c’est-à-dire que la valeur alpha ne pré-multiplie pas les valeurs des pixels), tandis que `tif-alpha` et `swf-alpha` renvoient la valeur alpha associée (c’est-à-dire que les valeurs alpha sont pré-multipliées avec les valeurs alpha). La couche alpha correspond à l’inverse du masque d’arrière-plan de la vignette pour `req=img`, et au masque de groupe ou d’objet s’il y a `req=object`. Pour appliquer la couche alpha lors de l’utilisation d’une requête infrarouge imbriquée, ajoutez des `fmt=` avec le format de fichier alpha approprié à la requête infrarouge incorporée et à la requête principale. Aucune donnée alpha n’est renvoyée si un profil ICC en CMJN ou en niveaux de gris est spécifié avec `icc=`.

## Propriétés {#section-eb12a82c69d84622bcea153dd84d95b3}

Peut se produire n’importe où dans la requête.

## Par défaut {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* La valeur par défaut est et `attribute::Format`*`tiffCompression`* la valeur par défaut sur `attribute::TiffEncoding`. *`pixelType`* La valeur par défaut est `rgb` si `icc=` n’est pas spécifiée, sinon elle correspond au type de pixels du profil ICC spécifié.

## Voir aussi {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute ::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [attribute ::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [attribute ::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb), [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
