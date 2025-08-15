---
title: Fmt
description: Format d’image de réponse.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: 67e12fae514341137e4218ea950f34da0d9997f3
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 2%

---

# Fmt{#fmt}

Format d’image de réponse.

`fmt=format[,``[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* – AVIF-alpha | AVIF | EPS | F4M | gif-alpha | GIF | heic | jpeg | JPEG2000-alpha | JPEG2000 | jpegxr-alpha | jpegxr | jpg | M3u8 | PDF | pjpeg | png-alpha | png | PNG8-alpha | PNG8 | SWF-alpha | SWF | SWF3-alpha | SWF3 | tif-alpha | tif | Web-alpha | WebP (en anglais)

| *`format`* | Description |
|---|---|
| `avif-alpha` | AVIF avec et sans perte avec couche alpha. |
| `avif` | AVIF avec et sans perte. |
| `eps` | Binaire non compressé Encapsulated PostScript. |
| `f4m` | Flash format de manifeste du serveur de flux continu. |
| `gif-alpha` | GIF avec 2 à 255 couleurs plus transparence des couleurs clés. |
| `gif` | GIF avec 2 à 256 couleurs. |
| `heic` | HEIC sans perte. Ce format est téléchargé par défaut à partir du navigateur s’il n’est pas pris en charge. |
| `jpeg` | JPEG avec perte. |
| `jpeg2000-alpha` | JPEG 2000 avec perte et sans perte avec couche alpha. |
| `jpeg2000` | JPEG 2000 avec et sans perte. |
| `jpegxr-alpha` | JPEG XR avec et sans perte avec couche alpha. |
| `jpegxr` | JPEG XR avec et sans perte. |
| `jpg` | JPG avec perte. |
| `m3u8` | Format de manifeste Apple Streaming Server. |
| `pdf` | Image incorporée au format PDF. |
| `pjpeg` | JPEG progressif. |
| `png-alpha` | PNG 24 bits sans perte avec couche alpha. |
| `png` | PNG 24 bits sans perte. |
| `png8-alpha` | PNG 8 bits sans perte avec couche alpha. |
| `png8` | PNG 8 bits sans perte. |
| `swf-alpha` | JPEG avec perte et masque compressé au format dégonflé incorporé dans un fichier SWF AS2 Adobe. |
| `swf` | JPEG avec perte incorporé dans un fichier SWF AS2 Adobe. |
| `swf3-alpha` | JPEG avec perte et masque compressé au format dégonflé incorporé dans un fichier SWF AS3 Adobe. **Remarque :** Les formats swf et swf-alpha sont mieux utilisés pour les applications ActionScript 2 (Flash Player 8 et versions antérieures). Les formats swf3 et swf3-alpha sont recommandés pour les applications ActionScript3 (Flash Player 9 et ultérieures). |
| `swf3` | JPEG avec perte incorporé dans un fichier SWF AS3 Adobe. |
| `tif-alpha` | TIFF avec couche alpha. |
| `tif` | BROUILLE. |
| `webp-alpha` | WebP avec et sans perte avec couche alpha. |
| `webp` | WebP avec et sans perte. |

*`pixelType`* – RVB | gris | Cmjn

| *`pixelType`* | Description |
|---|---|
| `cmyk` | Renvoie des données d’image CMJN. |
| `gray` | Renvoie des données d’image en niveaux de gris. |
| `rgb` | Renvoie des données d’image RVB. |

*`compression`* – jpeg | avec perte | Sans perte | LZW | Aucune | fermeture éclair

| *`compression`* | Description |
|---|---|
| `jpeg` | Compression JPEG (avec perte). |
| `lossy` | JPEG 2000, compression JPEG XR (avec perte) et WebP. |
| `lossless` | Compression HEIC, JPEG 2000 et JPEG XR (sans perte) et WebP. |
| `lzw` | Compression LZW (Lempel-Ziv-Welch) (sans perte). |
| `none` | Non compressé. |
| `zip` | Compression « Deflate » (sans perte). |

* *`format`* spécifie le format de codage d’image pour les données image envoyées au client et le type MIME de réponse correspondant pour l’en-tête de réponse HTTP.
* *`pixelType`* Peut être utilisé pour effectuer la conversion de l’espace colorimétrique de sortie lorsque `icc=` n’est pas spécifié.

  Le profil de couleur correspondant à *`pixelType`* est appliqué. Si la gestion des couleurs est désactivée, la conversion naïve est appliquée. *`pixelType`* est ignoré lorsque `icc=` est spécifié, ce qui détermine le type de pixel de sortie.

* *`compression`* n’est autorisée que si `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`, ou `jpegxr-alpha` est spécifié comme .*`format`* Reportez-vous au tableau ci-dessous pour connaître les options de compression prises en charge pour ces formats d’image.

Vous pouvez `qlt=` utiliser pour définir les options de codage JPEG pour les formats suivants : JPEG, TIFF avec compression JPEG, PDF avec compression JPEG et SWF. WebP, JPEG 2000 et JPEG XR utilisent `qlt=` également, mais les valeurs se traduisent par des qualités différentes pour les différents formats. Utilisez `quantize=` si `fmt=gif` ou `fmt=gif-alpha`. Reportez-vous aux descriptions des commandes pour plus d’informations. Les autres formats ne disposent pas d’options définissables.

8 bits par composant de pixel sont renvoyés pour tous les composants et *`formats`* (8 bits par pixel pour GIF *`pixelTypes`*).

Le tableau suivant répertorie les combinaisons valides de *`format`*et *`pixelType`*, les types MIME de réponse HTTP correspondants, si les profils ICC peuvent être incorporés (voir [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) et quelles options spécifiques au format vous pouvez appliquer.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b><i> format</i> </b> </th> 
   <th class="entry"> <b><i> Type de</i> pixel </b> </th> 
   <th class="entry"> <b> Type MIME de réponse</b> </th> 
   <th class="entry"> <b>Intégrer le profil ICC</b> </th> 
   <th class="entry"> <b> Options</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rvb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image vif=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"><span class="varname"> compression </span> </span> <span class="codeph">( avec perte </span>, <span class="codeph"> sans </span>perte ) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour <span class="codeph"> les fichiers sans </span>perte. </p> <p>Parce qu’il n’y a pas de concept de sous-échantillonnage de chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt = 80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> Eps </p> </td> 
   <td colname="col2"> <p>RVB, Gris, CMJN </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image ps=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>RVB, gris </p> <p>Les données sont converties en palette après conversion en gris ou RVB. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image if=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rvb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image eic=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Non </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>RVB, gris </p> </td> 
   <td> <p> <span class="codeph"> &lt;image p2=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"><span class="varname"> compression </span> </span> <span class="codeph">( avec perte </span>, <span class="codeph"> sans </span>perte ) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour <span class="codeph"> les fichiers sans </span>perte. </p> <p>Parce qu’il n’y a pas de concept de sous-échantillonnage de chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt = 80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>RVB, Gris, CMJN </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image peg=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>Le <span class="codeph"> paramètre pscan= </span> ne s’applique qu’au format pjpeg. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image nd.ms-photo=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"><span class="varname"> compression </span> </span> <span class="codeph">( avec perte </span>, <span class="codeph"> sans </span>perte ) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour <span class="codeph"> les fichiers sans </span>perte. </p> <p>Parce qu’il n’y a pas de concept de sous-échantillonnage de chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt = 80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>RVB, Gris, CMJN </p> </td> 
   <td colname="col3"> <p> <span class="codeph">&lt;application df=""&gt; </span>&lt;/application&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"><span class="varname"> compression </span> </span> <p> <span class="codeph">( none|zip|jpeg </span>), <span class="codeph"> qlt=</span> </p> <p> <span class="codeph">qlt= </span> est ignoré sauf si <span class="codeph"> <span class="varname"> la compression </span> </span> est définie sur <span class="codeph"> jpeg</span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rvb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image ng=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>RVB, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image ng=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>RVB, gris </p> </td> 
   <td colname="col3"> <p> <span class="codeph">&lt;application -shockwave-flash=""&gt; </span>&lt;/application&gt; </p> </td> 
   <td colname="col4"> <p>Non </p> <p> <p>Remarque : le Flash Player Adobe ignore les profils ICC incorporés. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute ::TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>RVB, Gris, CMJN </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image iff=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td colname="col4"> <p>Oui </p> </td> 
   <td colname="col5"> <span class="codeph"><span class="varname"> compression </span> </span> <p> <span class="codeph">( aucun|lzw|zip|jpeg </span>) </p> <p>« tiff » uniquement ; 'Tiff-alpha' ne prend pas en charge la compression JPEG. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> est ignoré sauf si <span class="varname"> la compression </span> est définie sur <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rvb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image ebp=""&gt; </span>&lt;/image&gt; </p> </td> 
   <td> <p>Non </p> </td> 
   <td> <p> <span class="codeph"><span class="varname"> compression </span> </span> <span class="codeph">( avec perte </span>, <span class="codeph"> sans </span>perte ) </p> <p> <span class="codeph"> qlt= </span> est ignoré pour <span class="codeph"> les fichiers sans </span>perte. </p> <p>Parce qu’il n’y a pas de concept de sous-échantillonnage de chrominance avec le format WebP, si vous utilisez une deuxième valeur avec <span class="codeph"> qlt </span> (par exemple, <span class="codeph"> qlt = 80,1 </span>), la deuxième valeur ( <span class="codeph"> 1 </span>) est ignorée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Attribut de requête. S’applique quel que soit le paramètre de calque actuel si `req=img` (par défaut) ou `req=mask`; ignoré dans le cas contraire.

*`type`* est ignoré si `iccProfile=` est spécifié.

## Par défaut {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, où l’objet *`defaultType`* est géré comme suit : Si `icc=` est spécifié, *`defaultType`* correspond au type de pixel du profil ICC spécifié. Si `icc=` n’est pas spécifié, *`defaultType`* est `gray` si `req=mask`, sinon c’est `rgb`.

## Exemples {#section-b93222e652df404a84c69025247f07df}

**Demande d’une petite image d’aperçu de faible qualité au format JPEG (par défaut) :**

` http:// *`serveur`*/myRootId/myImageId?qlt=60&wid=200`

**Demandez que la même image soit convertie en niveaux de gris :**

` http:// *`serveur`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Demandez la même image dans un format sans perte avec couche alpha et en haute résolution :**

` http:// *`serveur`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Demande la couche alpha pour la même image qu’une image TIFF en niveaux de gris :**

` http:// *`serveur`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Convertissez la même image en CMJN à l’aide des profils ICC par défaut :**

` http:// *`serveur`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Convertissez la même image en CMJN à l’aide d’un profil ICC différent et incorporez le profil dans l’image TIFF :**

` http:// *`serveur`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Fournissez cette image sous forme de fichier TIF avec compression JPEG sans conversion de type pixels :**

` http:// *`serveur`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Convertir l’image en GIF bi-tonal avec transparence des couleurs clés et forcer les couleurs en noir et blanc :**

` http:// *`serveur`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Lossy avec un paramètre de qualité de 80 :**

` http:// *`serveur`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sans perte avec alpha :**

` http:// *`serveur`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Lossy avec un paramètre de qualité de 80 :**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sans perte avec alpha :**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Lossy avec un paramètre de qualité de 80 :**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sans perte avec alpha :**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Voir aussi {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , quantize=[, req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)icc=[, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)iccEmbed=[, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)pathEmbed=[, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)pscan[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
