---
description: Les options suivantes peuvent être appliquées quel que soit le type de sourceFile.
seo-description: Les options suivantes peuvent être appliquées quel que soit le type de sourceFile.
seo-title: Options communes
solution: Experience Manager
title: Options communes
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Options communes{#common-options}

Les options suivantes peuvent être appliquées quel que soit le type de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> chaîne </span></span> </p> </td> 
  <td class="stentry"> <p>Dossier dans lequel les fichiers de sortie doivent être placés (y compris le fichier journal, si <span class="codeph"> -log </span> est spécifié). Peut être un chemin absolu ou relatif au répertoire de travail actuel. La hiérarchie des dossiers est créée si elle n’existe pas. Ne s’applique pas au fichier spécifié par <span class="codeph"> -log </span>. S’ils ne sont pas spécifiés, les fichiers de sortie sont écrits dans le dossier contenant le <span class="varname"> fichier source </span> . Si <span class="varname"> destFile </span> est spécifié, il sera toujours écrit à cet emplacement et <span class="codeph"> -destpath </span> s’applique uniquement aux fichiers de sortie secondaires. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Le cas échéant, la (première) image  du est extraite de la vignette, d’une image de panneau appropriée d’un style d’armoire ou de la première image d’éclairage d’un style de garniture de fenêtre. L’image extraite est enregistrée dans un fichier TIFF en pleine résolution. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Empêche la génération de fichiers . Utile pour extraire rapidement des attributs du <span class="varname"> fichier source </span>. Seules les vignettes facultatives ( <span class="codeph"> -thumbwidth </span>), les images ( <span class="codeph"> -image </span>) et les fichiers journaux ( <span class="codeph"> -log </span>) sont générés. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Sélectionne le codage JPEG avec perte pour les données d’image RVB et en niveaux de gris incorporées dans le fichier de sortie, plutôt que le format PNG sans perte. Les images au format alpha (RGBA) sont toujours enregistrées à l’aide du codage PNG. <span class="varname"> ival </span> spécifie la qualité JPEG (1...100); 85 ou plus est recommandé. La valeur par défaut est <span class="codeph"> -jpegquality 0 </span>, qui sélectionne le codage PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> chemin </span></span> </p> </td> 
  <td class="stentry"> <p>Crée un fichier journal avec le chemin/nom spécifié Les chemins complets de tous les fichiers de sortie écrits dans le dossier de destination sont écrits dans le fichier journal, ainsi que certains paramètres supplémentaires, tels que les informations de version et les avertissements ou erreurs rencontrés (voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> pour plus de détails). Aucun fichier journal n'est créé si <span class="codeph"> -log </span> n'est pas spécifié ; dans ce cas, toute la sortie de texte est écrite dans <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Réduisez la priorité du processus <span class="filepath"> vntc </span> . Vous pouvez l'utiliser pour que <span class="filepath"> vntc </span> ne prenne pas en charge l'intégralité du processeur lors du traitement d'une vignette. Cela permet au système d'exploitation de donner plus de temps à d'autres processus, plus importants. <span class="varname"> ival </span> indique le pourcentage de priorité inférieur (0.100). La valeur par défaut est <span class="codeph"> -lowerpriority 0 </span>, ce qui ne diminue pas la priorité du <span class="filepath"> processus vntc </span> . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Spécifiez la quantité maximale de mémoire que <span class="filepath"> vntc </span> est autorisé à utiliser en octets. Lorsque <span class="filepath"> vntc </span> atteint la limite de mémoire maximale, il arrête le traitement et génère une erreur. <span class="varname"> ival </span> spécifie la limite de mémoire maximale en octets (0. 3.758.096.384 (3,5 Go)). Lorsque <span class="varname"> la valeur </span> est 0, la limite de mémoire maximale est désactivée. La valeur par défaut est <span class="codeph"> -maxmem 3221225472 </span>, ce qui signifie une limite de mémoire maximale de 3 Go. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>Indique le séparateur placé entre le nom de fichier et le suffixe taille/résolution pour les noms de fichiers de sortie générés automatiquement. La valeur par défaut est "-" si elle n’est pas spécifiée. Ignoré si <span class="varname"> destFile </span> ou <span class="codeph"> -info </span> est spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Permet l’accentuation des images rééchantillonnées (mises à l’échelle) pendant le traitement. S’applique uniquement à l’accentuation des miniatures dans le cas de fichiers de style CAB. </p> <p>Spécifiez 0 pour désactiver l’accentuation (par défaut), 1 pour activer l’accentuation normale, 2 pour activer le masquage flou uniquement pour la luminosité, ou 3 pour activer le masquage flou pour chaque composante de couleur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelel </span> </p> </td> 
  <td class="stentry"> <p>Définit le niveau du journal. La valeur par défaut est 1, ce qui génère tous les messages d’informations, d’avertissement et d’erreur. Définissez cette variable sur 0 pour désactiver tous les messages sauf les messages d’erreur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> quantité </span> de rayon <span class="varname"> seuil </span> de rayon <span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>Définit les paramètres de masquage flou. Ignoré si <span class="codeph"> -sharpen </span> est défini sur 0 ou 1 ; requise si <span class="codeph"> -sharpen </span> est défini sur 2 ou 3. <span class="varname"> amount </span> est une valeur réelle dans la plage 0.0...500.0, <span class="varname"> radius </span> est une valeur réelle dans la plage 0.0...10.0 et le seuil <span class="varname"> </span> est un entier compris entre 0 et 255. Pour plus d’informations, consultez la description de <span class="codeph"> op_usm= </span> dans le Guide de référence du protocole de diffusion d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Vérifiez que la vignette indiquée est une vignette de production appropriée. <span class="varname"> ival </span> représente la version minimale du fichier de la vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>Version du fichier de sortie. Le cas échéant, la valeur doit être 0 ou une version valide du fichier de vignette (pas plus grande que la version de fichier par défaut). Si cette valeur est définie sur 0 ou non, le fichier de sortie est créé à l’aide de la version de fichier la plus récente. Ignoré si <span class="codeph"> -info </span> est spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Renvoie des informations sur la version de cet utilitaire. Spécifiez sans nom de fichier ni autres options. </p> </td> 
 </tr> 
</table>

