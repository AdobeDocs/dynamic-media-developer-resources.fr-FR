---
description: Format d’image de réponse.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 4%

---


# fmt{#fmt}

Format d’image de réponse.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alpha | png8-alpha | tif | tif-alpha | swf | swf-alpha | swf3 | swf3-alpha | eps | gif | gif-alpha | m3u8 | f4m | web | webp-alpha | jpeg2000 | jpeg2000-alpha | jpegxr | jpegxr-alpha

| *`format`* | Description |
|---|---| 
| `jpeg` | JPEG avec perte |
| `jpg` | JPG avec perte |
| `pjpeg` | JPEG progressif |
| `png` | PNG 24 bits sans perte |
| `png8` | PNG 8 bits sans perte |
| `png-alpha` | PNG 24 bits sans perte avec canal alpha |
| `png8-alpha` | PNG 8 bits sans perte avec canal alpha |
| `tif` | TIFF |
| `tif-alpha` | TIFF avec canal alpha |
| `pdf` | Image incorporée dans le PDF |
| `eps` | PostScript encapsulé binaire non compressé |
| `gif` | GIF de 2 à 256 couleurs |
| `gif-alpha` | GIF de 2 à 255 couleurs + transparence de couleur clé |
| `swf` | JPEG avec perte incorporé dans un fichier swf AS2 Adobe |
| `swf-alpha` | JPEG avec perte et masque compressé avec déflation incorporés dans un fichier swf AS2 Adobe |
| `swf3` | JPEG avec perte incorporé dans un fichier swf AS3 Adobe |
| `swf3-alpha` | JPEG avec perte et masque compressé avec déflation incorporés dans un fichier swf AS3 Adobe. **Remarque** : les formats swf et swf-alpha sont mieux utilisés pour les applications ActionScript 2 (Flash Player 8 et versions antérieures). swf3 et swf3-alpha sont recommandés pour les applications ActionScript3 (Flash Player 9 et versions ultérieures) |
| `m3u8` | Format du manifeste Apple Streaming Server |
| `f4m` | Format du manifeste du serveur de flux continu Flash |
| `webp` | WebP sans perte et sans perte |
| `webp-alpha` | WebP sans perte et sans perte avec canal alpha |
| `jpeg2000` | JPEG 2000 sans perte |
| `jpeg2000-alpha` | JPEG 2000 sans perte et perte avec canal alpha |
| `jpegxr` | JPEG XR sans perte |
| `jpegxr-alpha` | JPEG XR sans perte avec canal alpha |


| *`pixelType`* — rvb | gris | cmyk |
| *`pixelType`* | Description |
|---|---|
| `rgb` | Renvoyer les données d’image RVB. |
| `gray` | Renvoie des données d’image en niveaux de gris. |
| `cmyk` | Renvoie les données d’image CMJN. |

| *`compression`* — none | lzw | zip | jpeg | perdant | sans perte |
| *`compression`* | Description |
|---|---|
| `none` | Non compressé |
| `lzw` | Compression LZW (Lempel-Ziv-Welch) (sans perte) |
| `zip` | Compression &quot;Deflate&quot; (sans perte) |
| `jpeg` | Compression JPEG (avec perte) |
| `lossy` | Compression WebP, JPEG 2000 et JPEG XR (avec perte) |
| `lossless` | Compression WebP, JPEG 2000 et JPEG XR (sans perte) |

* *`format`* spécifie le format de codage d’image pour les données d’image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.
* *`pixelType`* peut être utilisé pour effectuer une conversion de l’espace colorimétrique de sortie lorsque  `icc=` n’est pas spécifié.

   Le profil de couleurs par défaut correspondant à *`pixelType`* est appliqué. Si la gestion des couleurs est désactivée, une conversion naïve est appliquée. *`pixelType`* est ignorée lorsque  `icc=` est spécifiée, ce qui détermine le type de pixel de sortie.

* *`compression`* n’est autorisée que si  `tif`,  `tif-alpha`,  `pdf`,  `webp`,  `webp-alpha`,  `jpeg2000`,  `jpeg2000-alpha`,  ou  est spécifié comme étant l’.`jpegxr``jpegxr-alpha`*`format`* Reportez-vous au tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

Vous pouvez utiliser `qlt=` pour définir les options de codage JPEG pour ces formats : JPEG, TIFF avec compression JPEG, PDF avec compression JPEG et SWF. WebP, JPEG 2000 et JPEG XR utilisent également `qlt=`, mais les valeurs produisent des qualités différentes pour les différents formats. Utilisez `quantize=` si `fmt=gif` ou `fmt=gif-alpha`. Consultez les descriptions des commandes pour plus de détails. Les autres formats n’ont pas d’options configurables.

Un composant de 8 bits par pixel est renvoyé pour tous les éléments *`formats`* et *`pixelTypes`* (8 bits par pixel pour GIF).

Le tableau suivant liste les combinaisons valides de *`format`*et *`pixelType`*, les types MIME de réponse HTTP correspondants, si les profils ICC peuvent être incorporés (voir [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) et les options propres au format que vous pouvez appliquer.

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
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p>Le paramètre <span class="codeph"> pscan= </span> s'applique uniquement au format pjpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rvb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression  </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>"tiff" uniquement ; 'tiff-alpha' ne prend pas en charge la compression jpeg. </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> qlt=  </span> est ignoré, sauf si  <span class="varname"> la compression  </span> est définie sur  <span class="codeph"> jpeg  </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf, swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> <p> <p>Remarque :  Le Flash Player d’Adobe ignore les profils ICC incorporés. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> attribut::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compression  </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt=  </span> est ignoré, sauf si  <span class="codeph"> <span class="varname"> la compression  </span> </span> est définie sur  <span class="codeph"> jpeg  </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, gray, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, gris </p> <p>Les données sont converties en palette après conversion en gris ou en rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantifier=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, webp-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compression  </span> </span> (  <span class="codeph"> perte  </span>,  <span class="codeph"> sans perte  </span>) </p> <p> <span class="codeph"> qlt=  </span> est ignoré pour  <span class="codeph"> sans perte  </span>. </p> <p>Comme il n’existe aucun concept de sous-échantillonnage de chrominance avec le format WebP, si vous utilisez une seconde valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt=80,1 </span>), la seconde valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, gris </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p>Comme ci-dessus. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p>Comme ci-dessus. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Attribut de requête. S’applique indépendamment du paramètre de calque actif si `req=img` (valeur par défaut) ou `req=mask`; ignoré autrement.

*`type`* est ignoré si  `iccProfile=` est spécifié.

## Par défaut {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, où la  *`defaultType`* méthode est gérée comme suit : Si  `icc=` est spécifié,  *`defaultType`* correspond au type de pixel du profil ICC spécifié. Si `icc=` n&#39;est pas spécifié, *`defaultType`* est `gray` si `req=mask`, sinon il est `rgb`.

## Exemples {#section-b93222e652df404a84c69025247f07df}

**Demandez une petite image de prévisualisation de faible qualité au format JPEG (par défaut) :**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Demandez la même image convertie en niveaux de gris :**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Demandez la même image dans un format sans perte avec un canal alpha et à haute résolution :**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Demandez le canal alpha pour la même image qu’une image TIFF en niveaux de gris :**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convertir la même image en cmyk à l’aide des profils ICC par défaut :**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convertissez la même image en cmyk à l’aide d’un autre profil ICC et incorporez le profil dans l’image TIFF :**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Diffusez cette image sous la forme d’un fichier TIF avec compression JPEG sans conversion de type de pixel :**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convertir l’image en un fichier GIF bitonal avec transparence de couleur clé et forcer les couleurs en noir et blanc :**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Perte avec un paramètre de qualité de 80 :**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sans perte avec alpha :**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Perte avec un paramètre de qualité de 80 :**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sans perte avec alpha :**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Perte avec un paramètre de qualité de 80 :**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sans perte avec alpha :**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Voir aussi {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), iccEmbed=, pathEmbed=, pscan.[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)
