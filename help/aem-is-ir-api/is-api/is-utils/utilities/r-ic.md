---
description: Utilitaire de conversion d’image.
seo-description: Utilitaire de conversion d’image.
seo-title: ic
solution: Experience Manager
title: ic
topic: Scene7 Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: e0f8153b038446180ddad313e591828223ed31e9

---


# ic {#ic}

Utilitaire de conversion d’image.

`ic` est un outil de ligne de commande qui convertit les fichiers image au format TIFF Pyramid optimisé (PTIFF). Bien que le service d’images puisse traiter les images sans conversion, nous vous recommandons de convertir toutes les images de plus de 512 x 512 pixels au format PTIFF. Cette conversion garantit des performances optimales du serveur et une utilisation optimale des ressources et réduit les temps de réponse.

Il est recommandé que les fichiers PTIFF contenant du contenu photographique soient codés au format JPEG (indiquez `-jpegcompress`). Le contenu généré par ordinateur peut bénéficier d’une compression sans perte ( `-deflatecompress` ou `-lzwcompress`). A moins qu’une conversion de couleur ou de type de pixel ne soit nécessaire, les données d’image source JPEG sont transférées au fichier PTIFF sans décodage, afin d’éviter une dégradation de la qualité. Dans ce cas, les options de compression spécifiées s’appliquent uniquement aux niveaux de pyramide de résolution inférieure.

Si vous ne convertissez pas d’images volumineuses, vous n’avez pas à définir les paramètres qui contrôlent la quantité de mémoire à utiliser. Toutefois, si vous l’êtes, vous devez `ic` plus de mémoire en utilisant le `-maxmem` paramètre décrit ci-dessous. Une bonne règle de base pour calculer la quantité de mémoire requise est de multiplier la largeur de l’image par rapport à la hauteur de l’image par rapport au nombre d’. Par exemple, quatre pour une image RVB avec une valeur alpha multipliée par trois. En outre, si le  de est de 16 bits par composant au lieu de 8  le résultat final.

## Utilisation {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]` *`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]` *`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]` *`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i></span></span> </p> </td> 
   <td colname="col2"> <p>Options de commande (voir ci-dessous). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> Fichier <i>source</i></span></span> </p> </td> 
   <td colname="col2"> <p>Fichier image d’entrée unique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span></span> </p> </td> 
   <td colname="col2"> <p>Fichier PTIFF de sortie unique (non valide s'il est utilisé avec SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>Dossier contenant des images d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>Dossier dans lequel les fichiers PTIFF de sortie sont écrits. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-36a2dcfa39824d29b69547c432366219}

0 en cas de succès. Si une erreur se produit, une valeur non nulle est renvoyée et les détails de l’erreur sont envoyés à `stderr`.

## Options {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -décompressé </span> </p> </td> 
   <td colname="col2"> <p>Ne compressez pas l’image de sortie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -déflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression compressée (zip) (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le codage JPEG. Ignoré si le <span class="codeph"> fichier <span class="varname"> source </span> </span> inclut des données alpha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Qualité JPEG (0-100; la valeur par défaut est 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Désactivez le sous-échantillonnage chromatique JPEG (ce qui peut améliorer la qualité du texte et des graphiques en couleur). Cela n’a aucun effet sur les images de sortie en CMJN ou en niveaux de gris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; <span class="varname"> seuil </span>&gt; &lt; <span class="varname"> monochrome &gt; </span></span> </p> </td> 
   <td colname="col2"> <p>Appliquer le masquage flou aux niveaux pyramidaux sous-échantillonnés. Voir <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> pour plus de détails. (Non appliqué à l’image en résolution complète.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le chemin d’accès à l’élément dans le fichier source, le cas échéant, pour créer les données alpha associées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Résolution d’impression (ppp) pour le <span class="codeph"> fichier <span class="varname"> de destination </span> </span>; si elle n’est pas spécifiée, la résolution d’impression de <span class="codeph"> srcFile </span> est copiée dans le <span class="codeph"> fichier <span class="varname"> de destination </span></span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autoculture &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> tolérance </span><span class="varname"> &gt; &lt; infoFichier &gt; </span></span> </p> </td> 
   <td colname="col2"> <p>Calculez un rectangle de recadrage pour minimiser l’arrière-plan en couleur unie. Aucune information de recadrage n’est générée si l’algorithme de recadrage automatique entraîne le rognage de l’image entière. </p> <p>Pour calculer le rectangle de recadrage sans convertir l’image, spécifiez <span class="codeph"> -autoculture </span> sans <span class="codeph"> -convertir </span> et sans <span class="codeph"> <span class="varname"> FichierDeDéfaut.</span> </span></p>

<p><i><b>coin</b></i> - ul| ur| ll| lr </p>
   <p> Indique le coin de l’image à utiliser comme point de départ. Ignoré si le mode est 1.</p>
   <p><i><b>mode</b></i> - 0| 1</p>
   <p>Définir sur 0 pour rogner en fonction de la couleur du pixel d'angle spécifié ; fonctionne sur des données de couleur prémultipliées si des données alpha sont associées à l’image source.</p>
   <p>Définir sur 1 pour le recadrage en fonction des données alpha ; corner est ignoré et 0 est toujours la valeur de départ ; aucun recadrage n’est appliqué si aucune donnée alpha n’est associée à l’image source.</p> 
   <p><i><b>tolérance</b></i> - Tolérance de correspondance. Valeur réelle comprise entre 0,0 et 1,0. Spécifie la tolérance pour les valeurs de composants de pixels correspondantes. Définissez sur 0 pour les correspondances exactes.</p>
   <p><i><b>infoFile</b></i> - Chemin et nom du fichier de sortie XML dans lequel seront écrites les données de recadrage.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Copiez les métadonnées XMP, le cas échéant, du <span class="codeph"> fichier <span class="varname"> source </span> vers le fichier </span> de destination <span class="codeph"> <span class="varname"> </span> sans modification.</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Incorporez le de couleurs ICC  dans le <span class="codeph"> fichier <span class="varname"> dest </span> </span>File, si disponible (aucun  de n’est incorporé par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin d’accès et nom d’un fichier  ICC. Définit l’espace colorimétrique du <span class="codeph"> fichier <span class="varname"> source </span> </span> et doit correspondre à son type de pixel. Doit être spécifié uniquement si aucune  de n’est incorporée dans le <span class="codeph"> fichier <span class="varname"> source </span> </span>, car elle remplace le  de incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin d’accès et nom d’un fichier  ICC. Définit le type de pixel et l’espace colorimétrique du <span class="codeph"> fichier <span class="varname"> principal </span> </span>. IC effectue une conversion vers ce si le <span class="codeph"> fichier <span class="varname"> source </span> contient un  de incorporé ou si le profil </span> -image <span class="codeph"> </span> est également spécifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu perceptif pour les conversions de l’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimétrie </span> </p> </td> 
   <td colname="col2"> <p> Mode de rendu Colorimétrique relatif pour les conversions d’espace colorimétrique (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimétrie </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu Colorimétrique absolu pour les conversions de l’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu de saturation pour les conversions de l’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Désactivation de la compensation des points noirs pour certaines conversions de couleurs </p> <p>Activé par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Désactivez le tramage (diffusion d’erreur) lors de la conversion des couleurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Désactivez la conversion automatique de CMJN en RVB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Forcer le décodage et le recodage des images d’entrée JPEG. </p> <p> <b>Attention :</b> L’application de cette option peut réduire la qualité de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le filtre de rééchantillonnage de qualité standard (bilinéaire). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de meilleure qualité (fenêtre Lanczos) (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de meilleure qualité (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubiicSharp </span> </p> </td> 
   <td colname="col2"> <p>Sous-échantillonner avec un filtre bicubique pointu de style Photoshop 8x8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nouge </span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’elle est spécifiée comme première option, supprime la sortie des informations d’utilisation lorsque des options non valides sont rencontrées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -remplacer </span> </p> </td> 
   <td colname="col2"> <p>Autoriser le remplacement d’un <span class="codeph"> fichier <span class="varname"> de destination existant </span> </span>. Par défaut, un suffixe numérique est ajouté au nom du fichier pour éviter tout écrasement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Ignorez les fichiers source masqués. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continue eonerror </span> </p> </td> 
   <td colname="col2"> <p>N’arrêtez pas le traitement en cas d’erreur. N’a un effet que lors du traitement de plusieurs fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> file </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin et nom du fichier journal (par défaut, <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Niveau de journal. </p> 
   <p>&lt; 0 - Journalisation désactivée.</p>
   <p>0 -  les fichiers à traiter.</p>
   <p>1 - Ajouter  pour les fichiers inutiles.</p>
   <p>2 - Ajouter de progrès .</p>
   <p>3 - Ajouter  sur chaque fichier rencontré.</p>
   <p>4 - Ajouter faire progresser le  au niveau du fichier.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>Ajouter au fichier journal (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Remplacer le fichier journal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogress msec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Intervalle de journalisation en msec pour le niveau de journalisation 2 et supérieur (3 000 par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite d’utilisation de la mémoire. Doit être d’au moins 10 Mo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite d’utilisation de la mémoire. La valeur par défaut est de 25 % de la mémoire physique. Si aucun <span class="codeph"> maxmem </span> ni <span class="codeph"> maxmempercent </span> ne sont explicitement définis, la valeur par défaut est maxmempercent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Informations de version renvoyées pour cet utilitaire. Spécifiez sans autres options. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formats d’image d’entrée pris en charge {#section-ab13d941d6724e65b9f84b62d949d31c}

Le tableau suivant  les options de format et de format des fichiers image prises en charge par IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Format</b> </p> </th> 
   <th class="entry"> <p> <b> Type</b> de pixels <b> bits/couche</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compression</b> </p> </th> 
   <th class="entry"> <p> <b> Remarques</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows Bitmap) </p> </td> 
   <td> <p> RVB| indexé </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> non compressé| RLE </p> </td> 
   <td> <p> 5/6 bits/ indique la prise en charge du RVB 16 bits (5-5-5 et 5-6-5 bits/). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Postscript encapsulé) </p> </td> 
   <td> <p> CMJN| RVB| gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII| ASCII85| Binary| JPEG </p> </td> 
   <td> <p> Seuls les fichiers EPS générés par Photoshop sont pris en charge. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> indexé </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> S’il est présent, la valeur de transparence de la palette est convertie en alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMJN| RVB| gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMJN| CMJN| RVB| RGBA| gris| grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> non compressé| compressé </p> </td> 
   <td> <p> Image fusionnée uniquement ; les calques et les  supplémentaires sont ignorés. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RVB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Données bitmap uniquement ; les données vectorielles sont ignorées. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RVB| RGBA| gris| grayA| indexé </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compressé </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMJN| CMJN| RVB| RGBA| gris| grayA| indexé </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> non compressé| ZIP| LZW| JPEG| RLE CCITT| CCITT G3| CCITT G4| Paquets </p> </td> 
   <td> <p> A l’exception du premier  alpha associé, les  de supplémentaires sont ignorées. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les  ICC incorporées sont reconnues dans les fichiers EPS, JPG, PSD, PNG et TIFF.

Les chemins incorporés et les métadonnées XMP sont reconnus dans les fichiers EPS, JPG, PSD et TIFF.

## Exemples {#section-3c1986b30315431989bd76b1ee5bef6d}

Convertissez une image unique de la meilleure qualité possible et conservez-la dans le même dossier :

`ic -convert src/myFile.png src/myFile.tif`

Convertir toutes les images *`srcFolder`* en fichiers TIFF pyramidaux codés JPEG et les placer dans *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convertir toutes les images dans *`srcFolder`*. Les données d’image codées des fichiers JPG sont utilisées pour la compression LZW en pleine résolution et sans perte pour le reste de la pyramide d’images de ces images ainsi que pour l’image de sortie complète de tous les fichiers d’entrée non JPG. Types de pixels,  de couleurs incorporées, métadonnées XMP, etc. sont conservées.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
