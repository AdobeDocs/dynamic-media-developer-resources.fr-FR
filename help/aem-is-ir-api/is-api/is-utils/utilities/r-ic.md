---
description: Utilitaire de conversion d’images.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1239'
ht-degree: 0%

---

# ic {#ic}

Utilitaire de conversion d’images.

`ic` est un outil de ligne de commande qui convertit les fichiers image au format Pyramid TIFF optimisé (PTIFF). Bien que la diffusion d’images puisse traiter les images sans conversion, nous vous recommandons de convertir en PTIFF toutes les images dont la taille est supérieure à 512 x 512 pixels. Cette conversion garantit des performances de serveur et une utilisation des ressources optimales et réduit les temps de réponse.

Il est recommandé que les fichiers PTIFF contenant du contenu photographique soient codés en JPEG (spécifiez `-jpegcompress`). Les contenus générés par ordinateur peuvent bénéficier d’une compression sans perte (`-deflatecompress` ou `-lzwcompress`). À moins qu’une conversion de couleur ou de type pixel ne soit requise, les données d’image source JPEG sont transférées au PTIFF sans décodage, afin d’éviter une dégradation de la qualité. Dans ce cas, les options de compression spécifiées s&#39;appliquent uniquement aux niveaux pyramidaux de résolution inférieure.

Si vous ne convertissez pas de grandes images, il n’est pas nécessaire de définir les paramètres qui contrôlent la quantité de mémoire à utiliser. Cependant, si c’est le cas, allouez `ic` de mémoire supplémentaire à l’aide du paramètre `-maxmem` décrit ci-dessous. Une bonne règle de base pour calculer la quantité de mémoire requise est de multiplier la largeur de l&#39;image par la hauteur de l&#39;image par le nombre de canaux. Par exemple, quatre pour une image RGB avec un temps alpha de trois. En outre, si les canaux sont de 16 bits par composant au lieu de 8, le double du résultat final.

## Utilisation {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>options</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Options des commandes (voir ci-dessous). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Fichier image à entrée unique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Fichier PTIFF à sortie unique (non valide si utilisé avec SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Dossier contenant les images entrantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Dossier dans lequel les fichiers PTIFF de sortie sont écrits. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Renvoie {#section-36a2dcfa39824d29b69547c432366219}

0 en cas de réussite. Si une erreur se produit, une valeur différente de zéro est renvoyée et les détails de l’erreur sont envoyés à `stderr`.

## Options {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - </span> non compressé </p> </td> 
   <td colname="col2"> <p>Ne pas compresser l’image de sortie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression dégonflée (zip) (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez la compression Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Utilisez l’encodage JPEG. Ignoré si <span class="codeph"> <span class="varname"> sourceFile </span> </span> contient des données alpha. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> quality </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Qualité JPEG (0-100 ; la valeur par défaut est 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Désactivez le sous-échantillonnage de la couleur de JPEG (peut améliorer la qualité du texte et des graphiques en couleur). Cela n’a aucun effet sur les images de sortie en CMJN ou en niveaux de gris. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> quantité </span>&gt; &lt; <span class="varname"> rayon </span>&gt; &lt; <span class="varname"> seuil </span>&gt; &lt; <span class="varname"> monochrome </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Appliquez un masquage flou aux niveaux pyramidaux sous-échantillonnés. Voir <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> pour plus de détails. (Non appliqué à l’image en pleine résolution.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Utilisez le chemin d’accès de l’élément dans le fichier source, le cas échéant, pour créer les données alpha associées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Résolution d’impression (dpi) pour <span class="codeph"> <span class="varname"> de </span> destFile </span> ; si elle n’est pas spécifiée, la résolution d’impression de <span class="codeph"> </span> srcFile est copiée vers <span class="codeph"> <span class="varname"> </span> destFile </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autorecadrage &lt; <span class="varname"> corner </span>&gt; &lt; <span class="varname"> mode </span>&gt; &lt; <span class="varname"> tolérance </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Calculez un rectangle de recadrage pour minimiser un arrière-plan de couleur unie. Aucune information de recadrage n’est générée si l’algorithme de recadrage automatique entraîne le recadrage de l’image entière. </p> <p>Pour calculer le rectangle de recadrage sans convertir l’image, spécifiez <span class="codeph"> -autocrup </span> sans <span class="codeph"> -convert </span> et sans <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>corner</b></i> - ul | Url | ll | lr </p>
   <p> Indique l’angle de l’image à utiliser comme point de départ. Ignoré si le mode est 1.</p>
   <p><i><b>mode</b></i> - 0 | 1</p>
   <p>Définissez la valeur sur 0 pour recadrer en fonction de la couleur du pixel d’angle spécifié ; fonctionne sur des données de couleur prémultipliées si des données alpha sont associées à l’image source.</p>
   <p>Définissez la valeur sur 1 pour recadrer en fonction des données alpha ; le coin est ignoré et 0 est toujours la valeur de départ ; aucun recadrage n’est appliqué si aucune donnée alpha n’est associée à l’image source.</p> 
   <p><i><b>tolérance</b></i> - Tolérance de correspondance. Valeur réelle 0,0 à 1,0. Indique la tolérance pour la correspondance des valeurs des composants en pixels. Définissez-le sur 0 pour les correspondances exactes.</p>
   <p><i><b>infoFile</b></i> - Chemin et nom du fichier de sortie XML dans lequel les données d’informations de recadrage sont écrites.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Copiez les métadonnées XMP, le cas échéant, de <span class="codeph"> <span class="varname"> sourceFile </span> </span> vers <span class="codeph"> <span class="varname"> destFile </span> </span> sans modification. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Incorporez le profil de couleurs ICC dans <span class="codeph"> <span class="varname"> fichier destFile </span> </span>, le cas échéant (aucun profil n’est incorporé par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin et nom d’un fichier de profil ICC. Définit l’espace colorimétrique <span class="codeph"> <span class="varname"> sourceFile </span> et doit correspondre </span> type de pixel. Ne doit être spécifié que si aucun profil n’est incorporé dans <span class="codeph"> <span class="varname"> sourceFile </span> </span>, car il remplace le profil incorporé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin et nom d’un fichier de profil ICC. Définit le type de pixel et l’espace colorimétrique <span class="codeph"> <span class="varname"> de </span> destFile </span>. IC convertit ce profil si <span class="codeph"> <span class="varname"> sourceFile </span> </span> a un profil incorporé ou si <span class="codeph"> -imageprofile </span> est également spécifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu perceptuel pour les conversions d’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Mode de rendu colorimétrique relatif pour les conversions d’espace colorimétrique (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Intention de rendu de colorimétrie absolue pour les conversions d’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Mode de rendu de saturation pour les conversions d’espace colorimétrique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Désactiver la compensation des points noirs pour certaines conversions de couleurs </p> <p>Activé par défaut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Désactivez le tramage (diffusion d’erreur) lors de la conversion des couleurs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Désactivez la conversion automatique de CMJN vers RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Forcer le décodage et le recodage des images d’entrée JPEG. </p> <p> <b>Attention :</b> l'application de cette option peut diminuer la qualité de l'image. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Utiliser un filtre de rééchantillonnage de qualité standard (bi-linéaire). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de meilleure qualité (fenêtre de Lanczos) (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Utilisez un filtre de rééchantillonnage de meilleure qualité (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Sous-échantillon avec filtre bicubique aigu Photoshop style 8x8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’elle est spécifiée comme première option, supprime la sortie des informations d’utilisation lorsque des options non valides sont rencontrées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -overwrite </span> </p> </td> 
   <td colname="col2"> <p>Permet de remplacer un fichier <span class="codeph"> existant <span class="varname"> destFile </span> </span>. Par défaut, un suffixe numérique est ajouté au nom de fichier pour empêcher le remplacement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Ignorez les fichiers sources masqués. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>N’arrêtez pas le traitement en cas d’erreur. N’a d’effet que lors du traitement de plusieurs fichiers. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> fichier </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chemin et nom du fichier journal (par défaut, <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> level </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Niveau de log. </p> 
   <p>&lt; 0 - Journalisation désactivée.</p>
   <p>0 - Répertoriez les fichiers à traiter.</p>
   <p>1 - Ajoutez des rapports pour les fichiers inutiles.</p>
   <p>2 - Ajoutez un rapport de progression.</p>
   <p>3 - Ajoutez des rapports sur chaque fichier rencontré.</p>
   <p>4 - Ajoutez des rapports de progression au niveau des fichiers.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>Ajoutez au fichier journal (par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Remplacer le fichier journal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Intervalle de journalisation en ms pour le niveau de journalisation 2 et supérieur (3 000 par défaut). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> octets </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite d’utilisation de la mémoire. Doit contenir au moins 10 Mo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> percent </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite d’utilisation de la mémoire. La valeur par défaut est de 25 % de la mémoire physique. Si ni <span class="codeph"> maxmem </span> ni <span class="codeph"> maxmempercent </span> ne sont explicitement définis, utilise maxmempercent default. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Renvoyer les informations de version pour cet utilitaire. Spécifiez sans autre option. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formats D’Image D’Entrée Pris En Charge {#section-ab13d941d6724e65b9f84b62d949d31c}

Le tableau suivant répertorie les formats de fichiers image et les options de format pris en charge par IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> format </b> </p> </th> 
   <th class="entry"> <p> Type <b> Pixel </b> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> bits/canal</b> </p> </th> 
   <th class="entry"> <p> <b> Compression</b> </p> </th> 
   <th class="entry"> <p> <b> notes</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Bitmap Windows) </p> </td> 
   <td> <p> RGB | indexé </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> non compressé | RÈGLE </p> </td> 
   <td> <p> 5/6 bits/canal indique la prise en charge de RGB 16 bits (5-5-5 et 5-6-5 bits/canal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Postscript Encapsulé) </p> </td> 
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
   <td> <p> DROIT </p> </td> 
   <td> <p> Si elle est présente, la valeur de transparence de la palette est convertie en alpha. </p> </td> 
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
   <td> <p> CMJN | CMJA | RGB | RGBA | grise | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> non compressé | compressé </p> </td> 
   <td> <p> Image fusionnée uniquement : les calques et les canaux supplémentaires sont ignorés. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RVB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RÈGLE </p> </td> 
   <td> <p> Données bitmap uniquement ; données vectorielles ignorées. </p> </td> 
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
   <td> <p> CMJN | CMJA | RGB | RGBA | grise | grayA | indexé </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> non compressé | ZIP | DROIT | JPEG | RÈGLE CCITT | CCITT G3 | CCITT G4 | Packbits </p> </td> 
   <td> <p> A l’exception de la première couche alpha associée, les couches supplémentaires sont ignorées. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les profils ICC incorporés sont reconnus dans les fichiers EPS, JPG, PSD, PNG et TIFF.

Les chemins d’accès intégrés et les métadonnées XMP sont reconnus dans les fichiers EPS, JPG, PSD et TIFF.

## Exemples {#section-3c1986b30315431989bd76b1ee5bef6d}

Convertissez une image unique avec la meilleure qualité possible et conservez-la dans le même dossier :

`ic -convert src/myFile.png src/myFile.tif`

Convertissez toutes les images de *`srcFolder`* en TIFF pyramidaux codés en JPEG et placez-les dans *`destFolder`* :

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Convertissez toutes les images en *`srcFolder`*. Les données d’image codées des fichiers JPG sont utilisées pour la compression LZW sans perte et de niveau de résolution complet pour le reste de la pyramide d’images de ces images, ainsi que pour l’image de sortie complète de tous les fichiers d’entrée non JPG. Types de pixels, profils de couleurs incorporés, métadonnées XMP, etc. sont entretenues.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
