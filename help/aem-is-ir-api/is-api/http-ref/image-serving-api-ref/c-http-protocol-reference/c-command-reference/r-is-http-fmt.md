---
title: fmt
description: Format d’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 17ccca8fcf75eaa902527837d83b03776c1386b9
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 2%

---

# fmt{#fmt}

Format d’image de réponse.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | hic | jpeg | jpeg2000-alpha | jpeg2000 | jpegxx-alpha | jpegxx | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | Description |
|---|---|
| `avif-alpha` | AVIF avec couche alpha sans perte. |
| `avif` | AVIF sans perte. |
| `eps` | PostScript encapsulé binaire décompressé. |
| `f4m` | Format de manifeste du serveur de diffusion en continu de Flash. |
| `gif-alpha` | GIF de 2 à 255 couleurs plus transparence couleur-clé. |
| `gif` | GIF de 2 à 256 couleurs. |
| `heic` | HEIC sans perte. Ce format est téléchargé par défaut à partir du navigateur s’il n’est pas pris en charge. |
| `jpeg` | JPEG perdant. |
| `jpeg2000-alpha` | JPEG 2000 sans perte avec canal alpha. |
| `jpeg2000` | JPEG sans perte 2000. |
| `jpegxr-alpha` | XR JPEG sans perte et avec couche alpha. |
| `jpegxr` | XR JPEG sans perte. |
| `jpg` | JPG perdant. |
| `m3u8` | Format de manifeste du serveur de diffusion en continu Apple. |
| `pdf` | Image incorporée dans PDF. |
| `pjpeg` | JPEG progressif. |
| `png-alpha` | PNG 24 bits sans perte avec canal alpha. |
| `png` | PNG 24 bits sans perte. |
| `png8-alpha` | PNG 8 bits sans perte avec canal alpha. |
| `png8` | PNG 8 bits sans perte. |
| `swf-alpha` | JPEG de perte et masque compressé par déflation incorporés dans un fichier swf AS2 Adobe. |
| `swf` | JPEG de perte incorporé dans un fichier swf AS2 Adobe. |
| `swf3-alpha` | JPEG de perte et masque décompressé incorporé dans un fichier swf AS3 Adobe. **Remarque :** les formats swf et swf-alpha sont mieux utilisés pour les applications ActionScript 2 (Flash Player 8 et versions antérieures). Les formats swf3 et swf3-alpha sont recommandés pour les applications ActionScript3 (Flash Player 9 et versions ultérieures). |
| `swf3` | JPEG de perte incorporé dans un fichier swf AS3 Adobe. |
| `tif-alpha` | TIFF avec canal alpha. |
| `tif` | TIFF. |
| `webp-alpha` | WebP sans perte et avec canal alpha. |
| `webp` | WebP sans perte et sans perte. |

| *`pixelType`* - rgb | gris | cmyk |
| *`pixelType`* | Description |
|---|---|
| `cmyk` | Renvoie les données image CMJN. |
| `gray` | Renvoie les données image en niveaux de gris. |
| `rgb` | Renvoie les données image du RGB. |

| *`compression`* - jpeg | perte | lossless | lzw | aucun | zip |
| *`compression`* | Description |
|---|---|
| `jpeg` | Compression des JPEG (perte). |
| `lossy` | JPEG 2000, la compression XR JPEG (perte) et WebP. |
| `lossless` | Compression HEIC, JPEG 2000 et JPEG XR (sans perte) et WebP. |
| `lzw` | Compression LZW (Lempel-Ziv-Welch) (sans perte). |
| `none` | Décompressé. |
| `zip` | Compression &quot;Deflate&quot; (sans perte). |

* *`format`* spécifie le format de codage de l’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.
* *`pixelType`* peut être utilisé pour effectuer une conversion de l’espace colorimétrique de sortie lorsque `icc=` n’est pas spécifié.

  Le profil colorimétrique par défaut correspondant à *`pixelType`* est appliquée. Si la gestion des couleurs est désactivée, une conversion naïve est appliquée. *`pixelType`* est ignoré lorsque `icc=` est spécifié, qui détermine le type de pixel de sortie.

* *`compression`* est autorisé uniquement si `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`, ou `jpegxr-alpha` est spécifié comme *`format`*. Reportez-vous au tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

Vous pouvez utiliser `qlt=` pour définir les options de codage du JPEG pour ces formats : JPEG, TIFF avec compression du JPEG, PDF avec compression du JPEG et SWF. WebP, JPEG 2000 et JPEG XR utilisent également `qlt=` mais les valeurs génèrent des qualités différentes pour les différents formats. Utilisation `quantize=` if `fmt=gif` ou `fmt=gif-alpha`. Pour plus d’informations, reportez-vous aux descriptions de commande . Les autres formats ne comportent pas d’options définissables.

Le composant 8 bits par pixel est renvoyé pour tous les *`formats`* et *`pixelTypes`* (8 bits par pixel pour le GIF).

Le tableau suivant répertorie les combinaisons valides de *`format`*et *`pixelType`*, les types MIME de réponse HTTP correspondants, si les profils ICC peuvent être incorporés (voir [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) et les options spécifiques au format que vous pouvez appliquer.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Type MIME de réponse</b> </th> 
   <th class="entry"> <b>Incorporer le profil ICC</b> </th> 
   <th class="entry"> <b> Options</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>La variable <span class="codeph"> pscan= </span> s’applique uniquement au format pjpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rvb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>'tiff' uniquement ; 'tiff-alpha' ne prend pas en charge la compression jpeg. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> est ignoré sauf <span class="varname"> compression </span> est défini sur <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> <p> <p>Remarque : Le Flash Player Adobe ignore les profils ICC incorporés. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> est ignoré sauf <span class="codeph"> <span class="varname"> compression </span> </span> est défini sur <span class="codeph"> jpeg </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> <p>Les données sont converties en palette après la conversion en gris ou en rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantifier= </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> ( <span class="codeph"> perte </span>, <span class="codeph"> lossless </span>) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour <span class="codeph"> lossless </span>. </p> <p>Puisqu’il n’existe aucun concept de sous-échantillonnage de chrominance avec le format WebP, si vous utilisez une seconde valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt=80,1 </span>) de la seconde valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p>Comme ci-dessus. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxx, jpegxx-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p>Comme ci-dessus. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rvb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p>Comme ci-dessus. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Attribut de requête. S’applique quel que soit le paramètre de calque actif si `req=img` (par défaut) ou `req=mask`; ignorer le contraire.

*`type`* est ignoré si `iccProfile=` est spécifié.

## Par défaut {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, où la variable *`defaultType`* est géré comme suit : Si `icc=` est spécifié, *`defaultType`* correspond au type de pixel du profil ICC spécifié. If `icc=` n’est pas spécifié, *`defaultType`* is `gray` if `req=mask`, sinon il est `rgb`.

## Exemples {#section-b93222e652df404a84c69025247f07df}

**Demandez une petite image d’aperçu de faible qualité au format JPEG (par défaut) :**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Demandez la même image convertie en niveaux de gris :**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Demandez la même image dans un format sans perte avec canal alpha et à haute résolution :**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Demandez le canal alpha pour la même image qu&#39;une image de TIFF en niveaux de gris :**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convertissez la même image en cmyk à l’aide des profils ICC par défaut :**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convertissez la même image en cmyk à l’aide d’un autre profil ICC et incorporez le profil dans l’image de TIFF :**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Diffusez cette image en tant que fichier TIF avec compression de JPEG sans conversion de type pixel :**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convertir l’image en GIF bimensuel avec transparence couleur-clé et forcer les couleurs en noir et blanc :**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Perte avec un paramètre de qualité de 80 :**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Lossless with alpha :**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Perte avec un paramètre de qualité de 80 :**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Lossless with alpha :**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Perte avec un paramètre de qualité de 80 :**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Lossless with alpha :**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Voir aussi {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantifier=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
