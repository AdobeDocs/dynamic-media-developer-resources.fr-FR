---
description: Les options suivantes peuvent être appliquées quel que soit le type de sourceFile.
solution: Experience Manager
title: Options communes
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# Options communes{#common-options}

Les options suivantes peuvent être appliquées quel que soit le type de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath  <span class="varname"> string  </span> </span> </p> </td> 
  <td class="stentry"> <p>Dossier dans lequel les fichiers de sortie doivent être placés (y compris le fichier journal, si <span class="codeph"> -log </span> est spécifié). Il peut s’agir d’un chemin d’accès absolu ou relatif au répertoire de travail actuel. La hiérarchie de dossiers sera créée si elle n’existe pas. Ne s’applique pas au fichier spécifié par <span class="codeph"> -log </span>. Si elle n’est pas spécifiée, les fichiers de sortie sont écrits dans le dossier dans lequel se trouve <span class="varname"> sourceFile </span>. Si <span class="varname"> destFile </span> est spécifié, il sera toujours écrit à cet emplacement et <span class="codeph"> -destpath </span> s’applique uniquement aux fichiers de sortie secondaires. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Si spécifié, l’image de la (première) vue est extraite de la vignette, d’une image de panneau appropriée à partir d’un style de cabinet ou de la première image d’éclairage d’une fenêtre recouvrant le style. L’image extraite est enregistrée en tant que fichier TIFF pleine résolution. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Empêche la génération de fichiers cibles. Utile pour extraire rapidement les attributs de <span class="varname"> sourceFile </span>. Seules les miniatures facultatives ( <span class="codeph"> -thumbwidth </span>), les images ( <span class="codeph"> -image </span>) et les fichiers journaux ( <span class="codeph"> -log </span>) sont générés. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Sélectionne le codage JPEG avec perte pour les données d’image en niveaux de gris et RVB incorporées dans le fichier de sortie, au lieu de PNG sans perte. Les images avec couche alpha (RGBA) sont toujours enregistrées à l’aide du codage PNG. <span class="varname"> ival  </span> spécifie la qualité JPEG (1...100) ; Il est recommandé d’utiliser la version 85 ou ultérieure. La valeur par défaut est <span class="codeph"> -jpegquality 0 </span>, ce qui sélectionne l’encodage PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log  <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>Crée un fichier journal avec le chemin/nom spécifié. Les chemins complets de tous les fichiers de sortie écrits dans le dossier de destination sont écrits dans le fichier journal, ainsi que certains paramètres supplémentaires, tels que les informations de version et les avertissements ou erreurs rencontrés (voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Sortie </a> pour plus de détails). Aucun fichier journal n’est créé si <span class="codeph"> -log </span> n’est pas spécifié ; dans ce cas, toutes les sorties de texte sont écrites dans la balise <span class="codeph"> </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Réduisez la priorité du processus <span class="filepath"> vntc </span> . Vous pouvez l’utiliser de sorte que <span class="filepath"> vntc </span> ne prenne pas en charge l’intégralité d’un processeur lors du traitement d’une vignette. Il permet au système d’exploitation de donner plus de temps à d’autres processus plus importants. <span class="varname"> ival  </span> indique le pourcentage de priorité plus faible (0.100). La valeur par défaut est <span class="codeph"> -lowerpriority 0 </span>, ce qui ne réduit pas la priorité du processus <span class="filepath"> vntc </span> . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Spécifiez la quantité maximale de mémoire que <span class="filepath"> vntc </span> est autorisé à utiliser en octets. Lorsque <span class="filepath"> vntc </span> atteint la limite maximale de mémoire, il arrête le traitement et génère une erreur. <span class="varname"> ival  </span> spécifie la limite de mémoire maximale en octets (0.. 3 758 096 384 (3,5 Go). Lorsque <span class="varname"> ival </span> est égal à 0, la limite de mémoire maximale est désactivée. La valeur par défaut est <span class="codeph"> -maxmem 3221225472 </span>, ce qui signifie une limite de mémoire maximale de 3 Go. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "  <span class="varname"> string  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>Indique le séparateur placé entre le nom de fichier et le suffixe taille/résolution pour les noms de fichiers de sortie générés automatiquement. La valeur par défaut est "-" si elle n’est pas spécifiée. Ignoré si <span class="varname"> destFile </span> ou <span class="codeph"> -info </span> est spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Permet l’accentuation des images rééchantillonnées (mises à l’échelle) pendant le traitement. S’applique uniquement à l’accentuation des miniatures en cas de fichiers de style Cabinet. </p> <p>Spécifiez 0 pour désactiver l’accentuation (par défaut), 1 pour activer l’accentuation normale, 2 pour activer le masquage flou uniquement pour la luminosité, ou 3 pour activer le masquage flou pour chaque composant de couleur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>Définit le niveau de journal. La valeur par défaut est 1, ce qui génère tous les messages d’information, d’avertissement et d’erreur. Définissez cette variable sur 0 pour désactiver tous les messages d’erreur à l’exception de . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm  <span class="varname"> amount  </span> <span class="varname"> radius  </span> <span class="varname"> seuil  </span> </span> </p> </td> 
  <td class="stentry"> <p>Définit les paramètres de masquage flou. Ignoré si <span class="codeph"> -sharpen </span> est défini sur 0 ou 1 ; obligatoire si <span class="codeph"> -sharpen </span> est défini sur 2 ou 3. <span class="varname"> amount  </span> est une valeur réelle dans la plage 0.0..500.0,  <span class="varname"> radius  </span> est une valeur réelle dans la plage 0.0...10.0, et  <span class="varname"> seuil  </span> est un entier compris entre 0 et 255. Pour plus d’informations, reportez-vous à la description de <span class="codeph"> op_usm= </span> dans la référence du protocole de diffusion d’images. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Vérifiez que la vignette indiquée est une vignette de production appropriée. <span class="varname"> ival  </span> représente la version minimale du fichier de la vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Version du fichier de sortie. Si spécifié, doit être défini sur 0 ou une version de fichier de vignette valide (pas plus grande que la version de fichier par défaut). S’il est défini sur 0 ou non spécifié, le fichier de sortie est créé à l’aide de la version de fichier la plus récente. Ignoré si <span class="codeph"> -info </span> est spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les informations de version de cet utilitaire. Spécifiez sans nom de fichier et autres options. </p> </td> 
 </tr> 
</table>
