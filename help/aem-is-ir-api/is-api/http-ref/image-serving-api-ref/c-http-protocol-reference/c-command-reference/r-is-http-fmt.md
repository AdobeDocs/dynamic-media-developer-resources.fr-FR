---
title: fmt
description: Format d’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 2%

---

# fmt{#fmt}

Format d’image de réponse.

`fmt=format[,` `[`*`pixelType`*`]` `[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | heic | jpeg | jpeg2000-alpha | jpeg2000 | jpegar-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | Description |
|---|---|
| `avif-alpha` | AVIF avec perte et sans perte avec canal alpha. |
| `avif` | AVIF avec ou sans perte. |
| `eps` | PostScript encapsulée binaire non compressée. |
| `f4m` | Format de manifeste du serveur de streaming Flash. |
| `gif-alpha` | GIF avec 2 à 255 couleurs et une transparence des couleurs clés. |
| `gif` | GIF de 2 à 256 couleurs. |
| `heic` | HEIC sans perte. Ce format est téléchargé par défaut à partir du navigateur s’il n’est pas pris en charge. |
| `jpeg` | JPEG avec perte. |
| `jpeg2000-alpha` | JPEG 2000 avec canal alpha sans perte. |
| `jpeg2000` | JPEG 2000 sans perte. |
| `jpegxr-alpha` | JPEG XR avec canal alpha avec perte et sans perte |
| `jpegxr` | JPEG XR avec ou sans perte. |
| `jpg` | JPG avec perte. |
| `m3u8` | Format de manifeste du serveur de streaming Apple. |
| `pdf` | Image incorporée dans PDF. |
| `pjpeg` | JPEG progressive. |
| `png-alpha` | PNG 24 bits sans perte avec canal alpha. |
| `png` | PNG 24 bits sans perte. |
| `png8-alpha` | PNG 8 bits sans perte avec canal alpha. |
| `png8` | PNG sans perte 8 bits. |
| `swf-alpha` | JPEG avec perte et masque dégonflé compressé incorporé dans un fichier swf Adobe AS2. |
| `swf` | JPEG avec perte incorporée dans un fichier swf Adobe AS2. |
| `swf3-alpha` | JPEG avec perte et masque dégonflé compressé incorporé dans un fichier swf Adobe AS3. **Remarque :** les formats swf et swf-alpha sont particulièrement adaptés aux applications ActionScript 2 (Flash Player 8 et versions antérieures). Les formats swf3 et swf3-alpha sont recommandés pour une utilisation avec les applications ActionScript3 (Flash Player 9 et versions ultérieures). |
| `swf3` | JPEG avec perte incorporée dans un fichier swf Adobe AS3. |
| `tif-alpha` | TIFF avec couche alpha. |
| `tif` | TIFF. |
| `webp-alpha` | WebP avec perte et sans perte avec canal alpha. |
| `webp` | WebP avec ou sans perte. |

*`pixelType`* - rvb | grise | cmjn

| *`pixelType`* | Description |
|---|---|
| `cmyk` | Renvoyer les données d’image CMJN. |
| `gray` | Renvoie des données d’image en niveaux de gris. |
| `rgb` | Renvoyer les données d’image RGB. |

*`compression`* - jpeg | qui a des pertes | sans perte | Droit | aucun | fermeture éclair

| *`compression`* | Description |
|---|---|
| `jpeg` | Compression JPEG (avec perte). |
| `lossy` | JPEG 2000, compression JPEG XR (avec perte) et WebP. |
| `lossless` | compression (sans perte) HEIC, JPEG 2000 et JPEG XR et WebP. |
| `lzw` | Compression LZW (Lempel-Ziv-Welch) sans perte. |
| `none` | Non compressé. |
| `zip` | Compression « dégonflée » (sans perte). |

* *`format`* spécifie le format de codage d’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.
* *`pixelType`* peut être utilisé pour effectuer la conversion de l’espace colorimétrique de sortie lorsque `icc=` n’est pas spécifié.

  Le profil colorimétrique par défaut correspondant à *`pixelType`* est appliqué. Si la gestion des couleurs est désactivée, une conversion naïve est appliquée. *`pixelType`* est ignoré lorsque `icc=` est spécifié, ce qui détermine le type de pixel de sortie.

* *`compression`* n’est autorisé que si `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr` ou `jpegxr-alpha` est spécifié comme *`format`*. Consultez le tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

Vous pouvez utiliser `qlt=` pour définir les options de codage JPEG pour les formats suivants : JPEG, TIFF avec compression JPEG, PDF avec compression JPEG et SWF. WebP, JPEG 2000 et JPEG XR utilisent également `qlt=`, mais les valeurs donnent des qualités différentes pour les différents formats. Utilisez `quantize=` si `fmt=gif` ou `fmt=gif-alpha`. Reportez-vous à la description des commandes pour plus d’informations. Les autres formats ne comportent pas d’options définissables.

8 bits par composant de pixel sont renvoyés pour tous les *`formats`* et *`pixelTypes`* (8 bits par pixel pour GIF).

Le tableau suivant répertorie les combinaisons valides de *`format`* et *`pixelType`*, les types MIME de réponse HTTP correspondants, si les profils ICC peuvent être incorporés (voir [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) et quelles options spécifiques au format vous pouvez appliquer.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format </i> </b> </th> 
   <th class="entry"> <b> <i> pixelType </i> </b> </th> 
   <th class="entry"> Type MIME de réponse <b></b> </th> 
   <th class="entry"> <b>Incorporer le profil ICC</b> </th> 
   <th class="entry"> <b> Options</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rvb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> (<span class="codeph"> </span> avec perte, <span class="codeph"> sans perte </span>) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour les <span class="codeph"> sans perte </span>. </p> <p>Comme il n’existe pas de concept de sous-échantillonnage de la chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt=80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rvb, gris, cmjn </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rvb, gris </p> <p>Les données sont converties en palette après conversion en gris ou en rvb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rvb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rvb, gris </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> (<span class="codeph"> </span> avec perte, <span class="codeph"> sans perte </span>) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour les <span class="codeph"> sans perte </span>. </p> <p>Comme il n’existe pas de concept de sous-échantillonnage de la chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt=80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rvb, gris, cmjn </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>Le paramètre <span class="codeph"> pscan= </span> s’applique uniquement au format pjpeg. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> (<span class="codeph"> </span> avec perte, <span class="codeph"> sans perte </span>) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour les <span class="codeph"> sans perte </span>. </p> <p>Comme il n’existe pas de concept de sous-échantillonnage de la chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt=80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rvb, gris, cmjn </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> est ignoré sauf si <span class="codeph"> <span class="varname"> compression </span> </span> est définie sur <span class="codeph"> </span> jpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rvb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rvb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf, swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rvb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-chokwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> <p> <p>Remarque : le lecteur Flash Adobe ignore les profils ICC incorporés. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rvb, gris, cmjn </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>« tiff » uniquement ; « tiff-alpha » ne prend pas en charge la compression jpeg. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> est ignoré sauf si <span class="varname"> compression </span> est définie sur <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression </span> </span> (<span class="codeph"> </span> avec perte, <span class="codeph"> sans perte </span>) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour les <span class="codeph"> sans perte </span>. </p> <p>Comme il n’existe pas de concept de sous-échantillonnage de la chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt=80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Attribut de requête. S’applique indépendamment du paramètre de calque actuel si `req=img` (par défaut) ou `req=mask` ; ignoré dans le cas contraire.

*`type`* est ignoré si `iccProfile=` est spécifié.

## Par défaut {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, où le *`defaultType`* est géré comme suit : si `icc=` est spécifié, *`defaultType`* correspond au type de pixel du profil ICC spécifié. Si `icc=` n’est pas spécifié, *`defaultType`* est `gray` si `req=mask` ; dans le cas contraire, il est `rgb`.

## Exemples {#section-b93222e652df404a84c69025247f07df}

**Demander une petite image d’aperçu de faible qualité au format JPEG (par défaut) :**

` http:// *`serveur`*/myRootId/myImageId?qlt=60&wid=200`

**Demander la même image convertie en niveaux de gris :**

` http:// *`serveur`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Demander la même image dans un format sans perte avec canal alpha et à haute résolution :**

` http:// *`serveur`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Demandez la couche alpha pour la même image qu’une image TIFF en niveaux de gris :**

` http:// *`serveur`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convertissez la même image en cmjn à l’aide des profils ICC par défaut :**

` http:// *`serveur`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convertissez la même image en cmjn à l’aide d’un profil ICC différent et incorporez le profil dans l’image TIFF :**

` http:// *`serveur`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Diffusez cette image en tant que fichier TIF avec la compression JPEG sans conversion de type pixel :**

` http:// *`serveur`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convertissez l’image en GIF bicolore avec transparence des couleurs de touches et forcez les couleurs au noir et blanc :**

` http:// *`serveur`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Avec perte avec un paramètre de qualité de 80:**

` http:// *`serveur`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sans perte avec alpha:**

` http:// *`serveur`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Avec perte avec un paramètre de qualité de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sans perte avec alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Avec perte avec un paramètre de qualité de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sans perte avec alpha:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Voir aussi {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
