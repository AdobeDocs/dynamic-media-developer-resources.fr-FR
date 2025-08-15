---
title: Options courantes
description: Les options suivantes peuvent être appliquées quel que soit le type de sourceFile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Options courantes{#common-options}

Les options suivantes peuvent être appliquées quel que soit le type de sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> chaîne </span> </span> </p> </td> 
  <td class="stentry"> <p>Dossier dans lequel seront placés les fichiers de sortie (y compris le fichier journal, si <span class="codeph"> -log </span> est renseigné). Il peut s’agir d’un chemin absolu ou d’un chemin relatif vers le répertoire de travail actuel. La hiérarchie de dossiers est créée si elle n’existe pas, mais elle ne s’applique pas au fichier spécifié avec <span class="codeph"> -log </span>. S’ils ne sont pas spécifiés, les fichiers de sortie sont écrits dans le dossier dans lequel se trouve le <span class="varname"> sourceFile </span>. Si <span class="varname"> paramètre destFile </span> est spécifié, il est toujours écrit à cet emplacement et <span class="codeph"> -destpath </span> s'applique uniquement aux fichiers de sortie secondaires. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image </span> </p> </td> 
  <td class="stentry"> <p>Si spécifié, la (première) image de vue est extraite de la vignette, une image de panneau appropriée d'un style d'armoire ou la première image d'éclairage d'un style de couvre-fenêtre. L’image extraite est enregistrée en tant que fichier TIFF en pleine résolution. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Empêche la génération de fichiers cibles. Utile pour extraire rapidement des attributs d’une <span class="varname"> sourceFile </span>. Seules les miniatures facultatives ( <span class="codeph"> -thumbwidth </span>), les images ( <span class="codeph"> -image </span>) et les fichiers journaux ( <span class="codeph"> -log </span>) sont générés. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Sélectionne le codage JPEG avec perte pour les données d’image en niveaux de gris et RGB incorporées dans le fichier de sortie, au lieu du codage PNG sans perte. Les images avec la couche alpha (RGBA) sont toujours enregistrées en utilisant le codage PNG. <span class="varname">’</span> ival spécifie la qualité de JPEG (1...100) ; 85 ou une valeur supérieure est recommandée. La valeur par défaut est <span class="codeph"> -jpegquality 0 </span>, qui sélectionne le codage PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> chemin </span> </span> </p> </td> 
  <td class="stentry"> <p>Crée un fichier journal avec le chemin/nom spécifié. Les chemins d’accès complets de tous les fichiers de sortie écrits dans le dossier de destination sont écrits dans le fichier journal, ainsi que certains paramètres supplémentaires, tels que les informations de version et les avertissements ou erreurs rencontrés (voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> des </a> de sortie pour plus d’informations). Aucun fichier journal n'est créé si <span class="codeph"> -log </span> n'est pas spécifié ; dans ce cas, toute sortie de texte est écrite dans <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Diminuer la priorité du processus de <span class="filepath"> vntc </span>. Ce processus peut être utilisé afin que <span class="filepath"> </span> vntc ne prenne pas le contrôle d'un CPU entier lors du traitement d'une vignette. Il permet au système d’exploitation de donner plus de temps à d’autres processus plus importants. <span class="varname"> ival </span> indique le pourcentage de priorité le plus faible (0..100). La valeur par défaut est <span class="codeph"> -lowerpriority 0 </span>, ce qui ne diminue pas la priorité du processus <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> flacon </span> </span> </p> </td> 
  <td class="stentry"> <p>Spécifiez la quantité maximale de mémoire que <span class="filepath"> </span> vntc est autorisé à utiliser en octets. Lorsque <span class="filepath"> </span> vntc atteint la limite de mémoire maximale, il arrête le traitement et génère une erreur. La <span class="varname"> ival </span> spécifie la limite de mémoire maximale en octets (0.. 3 758 096 384 (3,5 Go). Lorsque <span class="varname">’</span> de fiole est 0, la limite maximale de la mémoire est désactivée. La valeur par défaut est <span class="codeph"> -maxmem 3221225472 </span>, ce qui signifie une limite de mémoire maximale de 3 Go. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator «  <span class="varname"> string </span> » </span> </p> </td> 
  <td class="stentry"> <p>Indique le séparateur placé entre le nom de fichier et le suffixe taille/résolution pour les noms de fichiers de sortie générés automatiquement. La valeur par défaut est « - » si elle n’est pas spécifiée. Ignoré si <span class="varname"> paramètre destFile </span> ou <span class="codeph"> -info </span> est spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - aiguisez <span class="varname"> flacon </span> </span> </p> </td> 
  <td class="stentry"> <p>Permet d’accentuer les images rééchantillonnées (mises à l’échelle) pendant le traitement. S’applique uniquement à l’accentuation des miniatures dans les fichiers de type armoire. </p> <p>Spécifiez 0 pour désactiver l’accentuation (par défaut), 1 pour activer l’accentuation normale, 2 pour activer l’accentuation uniquement pour la luminosité ou 3 pour activer l’accentuation pour chaque composant de couleur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Définit le niveau de journalisation. La valeur par défaut est 1, ce qui génère tous les messages d’information, d’avertissement et d’erreur. Définissez cette valeur sur 0 pour désactiver tous les messages, à l’exception des messages d’erreur. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> montant </span> <span class="varname"> rayon </span> <span class="varname"> seuil </span> </span> </p> </td> 
  <td class="stentry"> <p>Définit les paramètres de masquage flou. Ignoré si <span class="codeph"> option d’accentuation </span> est définie sur 0 ou 1 ; obligatoire si <span class="codeph"> option d’accentuation </span> est définie sur 2 ou 3. Le <span class="varname"> montant </span> est une valeur réelle dans la plage 0.0...500.0, le <span class="varname"> rayon </span> est une valeur réelle dans la plage 0.0...10.0, et le <span class="varname"> seuil </span> est un entier compris entre 0 et 255. Pour plus d’informations, consultez la description de <span class="codeph"> op_usm= </span> dans Référence du protocole de diffusion d’images . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Vérifiez que la vignette donnée est une vignette de production appropriée. La <span class="varname"> ival </span> représente la version de fichier minimale de la vignette. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Version du fichier de sortie. S’il est spécifié, il doit être égal à 0 ou à une version de fichier de vignette valide (pas plus grande que la version de fichier par défaut). S’il est défini sur 0 ou non spécifié, le fichier de sortie est créé à l’aide de la version de fichier la plus récente. Ignoré si <span class="codeph"> -info </span> est spécifié. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>Renvoie les informations de version pour cet utilitaire. Spécifiez sans nom de fichier ni autres options. </p> </td> 
 </tr> 
</table>
