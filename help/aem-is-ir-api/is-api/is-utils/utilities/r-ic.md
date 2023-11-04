---
description: Utilitaire de conversion d’images.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1204'
ht-degree: 1%

---

# ic {#ic}

Utilitaire de conversion d’images.

`ic` est un outil de ligne de commande qui convertit les fichiers image au format PTIFF (Pyramid TIFF) optimisé. Bien que la diffusion d’images puisse traiter les images sans conversion, nous vous recommandons de convertir toutes les images de plus de 512x512 pixels en PTIFF. Cette conversion permet d’optimiser les performances du serveur et l’utilisation des ressources, tout en réduisant les temps de réponse.

Il est recommandé que les fichiers PTIFF contenant du contenu photographique soient codés en JPEG (spécifiez `-jpegcompress`). Les contenus générés par l’ordinateur peuvent bénéficier d’une compression sans perte (soit `-deflatecompress` ou `-lzwcompress`). À moins d’une conversion de couleur ou d’une conversion de type pixel requise, les données d’image source du JPEG sont transférées au fichier PTIFF sans décodage, afin d’éviter une dégradation de la qualité. Dans ce cas, les options de compression spécifiées s’appliquent uniquement aux niveaux pyramidaux de résolution inférieure.

Si vous ne convertissez pas d’images volumineuses, il n’est pas nécessaire de définir les paramètres qui contrôlent la quantité de mémoire à utiliser. Cependant, si vous l’êtes, donnez `ic` plus de mémoire en utilisant la fonction `-maxmem` décrit ci-dessous. Une bonne règle de base pour calculer la quantité de mémoire requise consiste à multiplier la largeur de l’image par la hauteur de l’image par le nombre de canaux. Par exemple, quatre pour une image de RGB avec une couche alpha de trois. En outre, si les canaux sont 16 bits par composant au lieu de 8, le résultat final est le double.

## Utilisation {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Options de commande (voir ci-dessous). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Fichier image d’entrée unique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Fichier PTIFF de sortie unique (non valide s’il est utilisé avec SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Dossier contenant des images d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Dossier dans lequel les fichiers PTIFF de sortie sont écrits. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-36a2dcfa39824d29b69547c432366219}

0 en cas de réussite. Si une erreur se produit, une valeur non nulle est renvoyée et les détails de l’erreur sont envoyés à `stderr`.

## Options {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -décompressé </span> </p> </td> 
   <td colname="col2"> <p>Ne compresse pas l’image de sortie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression déflate (zip) (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le codage du JPEG. Ignoré si <span class="codeph"> <span class="varname"> sourceFile </span> </span> inclut des données alpha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> qualité </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Qualité du JPEG (0 à 100 ; la valeur par défaut est 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Désactivez le sous-échantillonnage chromatique JPEG (peut améliorer la qualité du texte et des graphiques en couleur). Cela n’a aucun effet sur les images de sortie CMJN ou niveaux de gris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; <span class="varname"> seuil </span>&gt; &lt; <span class="varname"> monochrome </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Appliquez un masquage flou aux niveaux de pyramide sous-échantillonnés. Voir <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> pour plus d’informations. (Non appliqué à l’image à résolution complète.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le chemin d’accès à l’élément dans le fichier source, le cas échéant, pour créer les données alpha associées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Résolution d’impression (ppp) pour <span class="codeph"> <span class="varname"> destFile </span> </span>; si elle n’est pas spécifiée, la résolution d’impression de <span class="codeph"> srcFile </span> est copié vers <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> tolérance </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Calculez un rectangle de recadrage afin de minimiser un arrière-plan en couleur uni. Aucune information de recadrage n’est générée si l’algorithme de recadrage automatique entraîne le recadrage de l’image entière. </p> <p>Pour calculer le rectangle de recadrage sans convertir l’image, spécifiez <span class="codeph"> -autocrop </span> without <span class="codeph"> -convert </span> et sans <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>corner</b></i> - ul | ur | tout | lr </p>
   <p> Indique le coin de l’image à utiliser comme point de départ. Ignoré si le mode est 1.</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>Définissez cette variable sur 0 pour effectuer un recadrage en fonction de la couleur du pixel d’angle spécifié ; fonctionne sur les données de couleur prémultipliées si des données alpha sont associées à l’image source.</p>
   <p>Définissez cette variable sur 1 pour effectuer un recadrage en fonction des données alpha ; un coin est ignoré et 0 est toujours la valeur de départ ; aucun recadrage n’est appliqué si aucune donnée alpha n’est associée à l’image source.</p> 
   <p><i><b>tolérance</b></i> - Tolérance de correspondance. Valeur réelle comprise entre 0,0 et 1,0. Spécifie la tolérance pour les valeurs de composant de pixel correspondantes. Définissez cette variable sur 0 pour connaître les correspondances exactes.</p>
   <p><i><b>infoFile</b></i> - Chemin et nom du fichier de sortie XML dans lequel les données d’informations de recadrage sont écrites.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Copie XMP métadonnées, le cas échéant, à partir de <span class="codeph"> <span class="varname"> sourceFile </span> </span> to <span class="codeph"> <span class="varname"> destFile </span> </span> sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Incorporation du profil de couleurs ICC dans <span class="codeph"> <span class="varname"> destFile </span> </span>, si disponible (aucun profil n’est incorporé par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin et nom d’un fichier de profil ICC. Définit l’espace colorimétrique de <span class="codeph"> <span class="varname"> sourceFile </span> </span> et doit correspondre à son type de pixel. Doit être spécifié uniquement si aucun profil n’est incorporé dans <span class="codeph"> <span class="varname"> sourceFile </span> </span>, car cela remplace le profil incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin et nom d’un fichier de profil ICC. Définit le type de pixel et l’espace colorimétrique de <span class="codeph"> <span class="varname"> destFile </span> </span>. IC convertit les données en ce profil si <span class="codeph"> <span class="varname"> sourceFile </span> </span> comporte un profil incorporé ou si <span class="codeph"> -imageprofile </span> est également spécifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerception </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu perceptuel pour les conversions de l’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Mode de rendu Colorimétrique relatif pour les conversions de l’espace colorimétrique (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu Colorimétrique absolu pour les conversions de l’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Intention de rendu de la saturation pour les conversions de l’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Désactivation de la compensation des points noirs pour certaines conversions de couleurs </p> <p>Activé par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Désactiver l’effet d’effet d’effet d’effet d’effet d’effet d’effet d’effet d’effet d’effet d’effet d’effet d’effet d’effet d’ombre (diffusion d’erreur) lors de la conversion des couleurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Désactivez la conversion automatique de CMJN en RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Forcer le décodage et le recodage des images d’entrée de JPEG. </p> <p> <b>Attention :</b> L’application de cette option peut réduire la qualité de l’image. </p> </td> 
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
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de meilleure qualité (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Sous-échantillonnez avec un filtre coupe-vis 8x8 de style Photoshop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nouge </span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’elle est spécifiée comme première option, supprime la sortie des informations d’utilisation lorsque des options non valides sont rencontrées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -remplacer </span> </p> </td> 
   <td colname="col2"> <p>Autoriser le remplacement d’un élément existant <span class="codeph"> <span class="varname"> destFile </span> </span>. Par défaut, un suffixe numérique est ajouté au nom du fichier pour éviter tout écrasement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Ignorer les fichiers source masqués. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>N’arrêtez pas le traitement en cas d’erreur. N’a un effet que lors du traitement de plusieurs fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin et nom du fichier journal (par défaut : <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Niveau de journal. </p> 
   <p>&lt; 0 - Journalisation désactivée.</p>
   <p>0 - Liste des fichiers à traiter.</p>
   <p>1 - Ajoutez un reporting pour les fichiers inutiles.</p>
   <p>2 - Ajoutez un rapport de progression.</p>
   <p>3 - Ajoutez un reporting sur chaque fichier rencontré.</p>
   <p>4 - Ajoutez un rapport de progression au niveau du fichier.</p>
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
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Intervalle de journalisation en msec pour le niveau de journalisation 2 et supérieur (la valeur par défaut est 3 000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> octets </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite d’utilisation de la mémoire. Doit contenir au moins 10 Mo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite d’utilisation de la mémoire. La valeur par défaut est de 25 % de la mémoire physique. Si aucun <span class="codeph"> maxmem </span> nor <span class="codeph"> maxmempercent </span> sont définis explicitement utilise la valeur par défaut maxmempercent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Informations sur la version renvoyée pour cet utilitaire. Spécifiez sans aucune autre option. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formats d’image d’entrée pris en charge {#section-ab13d941d6724e65b9f84b62d949d31c}

Le tableau suivant répertorie les formats de fichiers image et les options de format pris en charge par IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Format</b> </p> </th> 
   <th class="entry"> <p> <b> Type de pixel</b> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compression</b> </p> </th> 
   <th class="entry"> <p> <b> Remarques</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows Bitmap) </p> </td> 
   <td> <p> RGB | indexé </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> décompressé | RLE </p> </td> 
   <td> <p> 5/6 bits/canal indique la prise en charge du RGB 16 bits (5-5-5 et 5-6-5 bits/canal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Encapsulated Postscript) </p> </td> 
   <td> <p> CMJN | RGB | grise </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binaire | JPEG </p> </td> 
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
   <td> <p> Si elle est présente, la valeur de transparence de la palette est convertie en valeur alpha. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMJN | RGB | grise </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMJN | CMJN | RGB | RGBA | grise | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> décompressé | compressé </p> </td> 
   <td> <p> Image fusionnée uniquement ; les calques et les autres canaux sont ignorés. </p> </td> 
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
   <td> <p> RGB | RGBA | grise | grayA | indexé </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compressé </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMJN | CMJN | RGB | RGBA | grise | grayA | indexé </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> décompressé | ZIP | LZW | JPEG | RLE CCITT | CCITT G3 | CCITT G4 | Packages </p> </td> 
   <td> <p> A l’exception du premier canal alpha associé, les canaux supplémentaires sont ignorés. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les profils ICC incorporés sont reconnus dans les fichiers EPS, JPG, PSD, PNG et TIFF.

Les chemins d’accès et les métadonnées XMP incorporés sont reconnus dans les fichiers EPS, JPG, PSD et TIFF.

## Exemples {#section-3c1986b30315431989bd76b1ee5bef6d}

Convertissez une seule image avec la meilleure qualité possible et conservez-la dans le même dossier :

`ic -convert src/myFile.png src/myFile.tif`

Convertir toutes les images dans *`srcFolder`* aux TIFFs pyramidaux codés en JPEG et placez-les dans *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convertir toutes les images dans *`srcFolder`*. Les données d’image codées des fichiers de JPG sont utilisées pour la compression LZW sans perte de niveau résolution totale pour le reste de la pyramide des images de ces images, ainsi que pour l’image de sortie complète de tous les fichiers d’entrée non JPG. Types de pixels, profils de couleurs incorporés, métadonnées XMP, etc. sont conservées.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
