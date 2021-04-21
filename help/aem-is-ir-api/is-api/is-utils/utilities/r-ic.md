---
description: Utilitaire de conversion d’image.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 2%

---


# ic {#ic}

Utilitaire de conversion d’image.

`ic` est un outil de ligne de commande qui convertit les fichiers image au format TIFF pyramidal optimisé (PTIFF). Bien que la diffusion d’images puisse traiter les images sans conversion, il est recommandé de convertir toutes les images de plus de 512 x 512 pixels au format PTIFF. Cette conversion garantit des performances optimales du serveur et une utilisation optimale des ressources et réduit les temps de réponse.

Il est recommandé que les fichiers PTIFF contenant du contenu photographique soient codés au format JPEG (indiquez `-jpegcompress`). Le contenu généré par l&#39;ordinateur peut bénéficier d&#39;une compression sans perte (soit `-deflatecompress` soit `-lzwcompress`). A moins d’une conversion de couleur ou d’une conversion de type de pixel requise, les données d’image source JPEG sont transférées au fichier PTIFF sans décodage, afin d’éviter toute dégradation de la qualité. Dans ce cas, les options de compression spécifiées s&#39;appliquent uniquement aux niveaux pyramidaux de résolution inférieure.

Si vous ne convertissez pas d’images volumineuses, il n’est pas nécessaire de définir les paramètres qui contrôlent la quantité de mémoire à utiliser. Cependant, si vous le faites, donnez `ic` plus de mémoire en utilisant le paramètre `-maxmem` décrit ci-dessous. Une bonne règle de base pour calculer la quantité de mémoire requise est de multiplier la largeur de l’image par la hauteur de l’image par le nombre de canaux. Par exemple, quatre pour une image RVB avec alpha multiplié par trois. De plus, si les canaux sont de 16 bits par composant au lieu de 8 doublons, le résultat final est obtenu.

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
   <td colname="col2"> <p>Fichier PTIFF de sortie unique (non valide s'il est utilisé avec SourceDirectory). </p> </td> 
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

0 en cas de réussite. Si une erreur se produit, une valeur non nulle est renvoyée et les détails de l&#39;erreur sont envoyés à `stderr`.

## Options {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -décompressé </span> </p> </td> 
   <td colname="col2"> <p>Ne compressez pas l’image de sortie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dégatecompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression déflate (zip) (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le codage JPEG. Ignoré si <span class="codeph"> <span class="varname"> sourceFile </span> </span> contient des données alpha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Qualité JPEG (0-100 ; par défaut : 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fulléchantillechrominance  </span> </p> </td> 
   <td colname="col2"> <p>Désactivez le sous-échantillonnage chromatique JPEG (ce qui peut améliorer la qualité du texte et des graphiques en couleur). Cela n’a aucun effet sur les images de sortie en CMJN ou en niveaux de gris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt;  &lt;&gt; seuil  </span>&gt;  &lt;&gt; monochrome &gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"></span> </span></span></span></p> </td> 
   <td colname="col2"> <p>Appliquer un masquage flou aux niveaux pyramidaux sous-échantillonnés. Voir <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> pour plus de détails. (Non appliqué à l’image à résolution complète.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le chemin d’accès à l’élément dans le fichier source, le cas échéant, pour créer les données alpha associées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Résolution d’impression (ppp) pour <span class="codeph"> <span class="varname"> destFile </span> </span>; si elle n’est pas spécifiée, la résolution d’impression de <span class="codeph"> srcFile </span> est copiée dans <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autoculture  &lt;&gt; corner  </span>&gt;  &lt;&gt; mode  </span>&gt;  &lt;&gt; tolérance  </span>&gt;  &lt;&gt; infoFile &gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"></span> </span></span></span></p> </td> 
   <td colname="col2"> <p>Calculez un rectangle de recadrage afin de minimiser l’arrière-plan en couleur unie. Aucune information de recadrage n’est générée si l’algorithme de recadrage automatique entraîne le rognage de l’image entière. </p> <p>Pour calculer le rectangle de recadrage sans convertir l’image, spécifiez <span class="codeph"> -autoculture </span> sans <span class="codeph"> -convert </span> et sans <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>coin</b></i> - ul | ur | all | lr </p>
   <p> Indique le coin de l’image à utiliser comme point de départ. Ignoré si le mode est 1.</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>Définir sur 0 pour rogner en fonction de la couleur du pixel d'angle spécifié ; fonctionne sur des données de couleur prémultipliées si des données alpha sont associées à l’image source.</p>
   <p>Définir sur 1 pour le recadrage en fonction des données alpha ; corner est ignoré et 0 est toujours la valeur de départ ; aucun recadrage n’est appliqué si aucune donnée alpha n’est associée à l’image source.</p> 
   <p><i><b>tolérance</b></i>  - Tolérance de correspondance. Valeur réelle comprise entre 0,0 et 1,0. Indique la tolérance pour les valeurs de composants de pixels correspondantes. Définissez sur 0 pour les correspondances exactes.</p>
   <p><i><b>infoFile</b></i>  : chemin et nom du fichier de sortie XML vers lequel les données d'information de recadrage seront écrites.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>Copiez XMP métadonnées, le cas échéant, de <span class="codeph"> <span class="varname"> sourceFile </span> </span> à <span class="codeph"> <span class="varname"> destFile </span> </span> sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> Incorporez le profil de couleurs ICC dans <span class="codeph"> <span class="varname"> destFile </span> </span>, si disponible (aucun profil n’est incorporé par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Chemin d’accès et nom d’un fichier de profil ICC. Définit l’espace colorimétrique de <span class="codeph"> <span class="varname"> sourceFile </span> </span> et doit correspondre à son type de pixel. Doit être spécifié uniquement si aucun profil n'est incorporé dans <span class="codeph"> <span class="varname"> sourceFile </span> </span>, car cela remplace le profil incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Chemin d’accès et nom d’un fichier de profil ICC. Définit le type de pixel et l’espace colorimétrique de <span class="codeph"> <span class="varname"> destFile </span> </span>. IC effectue une conversion vers ce profil si <span class="codeph"> <span class="varname"> sourceFile </span> </span> comporte un profil incorporé ou si <span class="codeph"> -imageprofile </span> est également spécifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerception  </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu perceptif pour les conversions d’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric  </span> </p> </td> 
   <td colname="col2"> <p> Mode de rendu Colorimétrique relatif pour les conversions d’espace colorimétrique (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimétrie  </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu Colorimétrique absolu pour les conversions d’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu de saturation pour les conversions d’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation  </span> </p> </td> 
   <td colname="col2"> <p>Désactiver la compensation des points noirs pour certaines conversions de couleur </p> <p>Activé par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>Désactivez l’effet de tramage (diffusion d’erreurs) lors de la conversion des couleurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype  </span> </p> </td> 
   <td colname="col2"> <p> Désactivez la conversion automatique de CMJN en RVB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>Force le décodage et le recodage des images d’entrée JPEG. </p> <p> <b>Attention : L’</b> application de cette option peut réduire la qualité de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de qualité standard (bilinéaire). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de meilleure qualité (fenêtre Lanczos) (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de meilleure qualité (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubiicSharp  </span> </p> </td> 
   <td colname="col2"> <p>Sous-échantillonner avec un filtre pointu bicubique 8x8 de style Photoshop. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> Lorsqu'elle est spécifiée comme première option, supprime la sortie des informations d'utilisation lorsque des options non valides sont rencontrées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -remplacer </span> </p> </td> 
   <td colname="col2"> <p>Permettre de remplacer un <span class="codeph"> <span class="varname"> destFile </span> </span> existant. Par défaut, un suffixe numérique est ajouté au nom du fichier pour éviter tout écrasement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiidden  </span> </p> </td> 
   <td colname="col2"> <p>Ignorez les fichiers source masqués. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror  </span> </p> </td> 
   <td colname="col2"> <p>N’arrêtez pas le traitement en cas d’erreur. N’a un effet que lors du traitement de plusieurs fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Chemin et nom du fichier journal (par défaut <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel  &lt;&gt; level  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Niveau de journal. </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 - Fichiers de Liste à traiter.</p>
   <p>1 - Ajouter le rapports pour les fichiers inutiles.</p>
   <p>2 - Ajouter le rapports de progrès.</p>
   <p>3 - Ajoutez le rapports sur chaque fichier rencontré.</p>
   <p>4 - Ajouter le rapports de progression au niveau du fichier.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>Ajouter au fichier journal (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>Remplacer le fichier journal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogress msec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Intervalle de journalisation en msec pour le niveau de journalisation 2 et supérieur (3000 par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; bytes  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Limite d'utilisation de la mémoire. Doit être d'au moins 10 Mo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent  &lt;&gt; percent  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Limite d'utilisation de la mémoire. La valeur par défaut est de 25 % de la mémoire physique. Si aucun <span class="codeph"> maxmem </span> ou <span class="codeph"> maxmempercent </span> n'est explicitement défini, maxmempercent utilise maxmempercent par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Informations de version renvoyées pour cet utilitaire. N’indiquez aucune autre option. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formats d’image d’entrée pris en charge {#section-ab13d941d6724e65b9f84b62d949d31c}

Le tableau suivant liste les formats de fichier image et les options de format pris en charge par IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Format</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel </b> <b> TypeBits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compression</b> </p> </th> 
   <th class="entry"> <p> <b> Remarques</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Windows Bitmap) </p> </td> 
   <td> <p> RVB | indexé </p> </td> 
   <td> <p> 3 | 5/6 | 8 </p> </td> 
   <td> <p> non compressé | RLE </p> </td> 
   <td> <p> 5/6 bits/canal indique la prise en charge du RVB 16 bits (5-5-5 et 5-6-5 bits/canal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Postscript encapsulé) </p> </td> 
   <td> <p> CMJN | RGB | gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | binaire | JPEG </p> </td> 
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
   <td> <p> CMJN | RGB | gris </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMJN | CMJN | RGB | RGBA | gris | grayA </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> non compressé | compressé </p> </td> 
   <td> <p> Image fusionnée uniquement ; les calques et les canaux supplémentaires sont ignorés. </p> </td> 
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
   <td> <p> RVB | RGBA | gris | grayA | indexé </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compressé </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMJN | CMJN | RGB | RGBA | gris | grayA | indexé </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> non compressé | ZIP | LZW | JPEG | RLE CCITT | CCITT G3 | CCITT G4 | Paquets </p> </td> 
   <td> <p> À l’exception du premier canal alpha associé, les canaux supplémentaires sont ignorés. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les profils ICC incorporés sont reconnus dans les fichiers EPS, JPG, PSD, PNG et TIFF.

Les chemins incorporés et les métadonnées XMP sont reconnus dans les fichiers EPS, JPG, PSD et TIFF.

## Exemples {#section-3c1986b30315431989bd76b1ee5bef6d}

Convertissez une image unique de la meilleure qualité possible et conservez-la dans le même dossier :

`ic -convert src/myFile.png src/myFile.tif`

Convertir toutes les images de *`srcFolder`* en TIFF pyramidaux codés JPEG et les placer dans *`destFolder`* :

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convertir toutes les images dans *`srcFolder`*. Les données d’image codées des fichiers JPG sont utilisées pour la compression LZW sans perte de résolution totale pour le reste de la pyramide d’images de ces images ainsi que pour l’image de sortie complète de tous les fichiers d’entrée non JPG. Types de pixels, profils de couleurs intégrés, métadonnées XMP, etc. sont conservées.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
