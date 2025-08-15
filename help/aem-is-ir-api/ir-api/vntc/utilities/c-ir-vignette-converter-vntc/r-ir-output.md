---
description: vntc génère des données textuelles qui sont envoyées à stderr ou au fichier journal.
solution: Experience Manager
title: Sortie
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Sortie{#output}

vntc génère des données textuelles qui sont envoyées à stderr ou au fichier journal.

Les données sont formatées en tant que propriété `name=value` par enregistrement de texte. Les valeurs de chaîne ne sont pas citées. Les messages d&#39;avertissement et d&#39;erreur sont toujours envoyés à `stderr`, même si `-log` est spécifié.

Certaines propriétés peuvent se produire plusieurs fois dans la même sortie. Un numéro de séquence, commençant par 0, est ajouté au nom de ces propriétés, séparé par un point. Ces propriétés sont identifiées ci-dessous avec un suffixe `. *`n`*` après le nom de la propriété.

Les propriétés suivantes sont générées :

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Couleur d’arrière-plan RGB du style d’armoire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Version du fichier de sortie par défaut. Cette version de vntc<span class="filepath"> peut également générer </span> numéro de version de fichier le plus élevé. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">erreur.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Message d’erreur. La présence de messages d’erreur indique généralement qu’aucun fichier de sortie n’est créé ou qu’ils ne peuvent pas être utilisés par le rendu d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>fichier <span class="codeph">.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Chemin/nom complet de tous les fichiers de sortie, y compris les vignettes, les fichiers de style armoire, les images en pleine résolution et les images miniatures. Un attribut de fichier est présent pour chaque fichier généré (à l’exception du fichier journal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">verre=<span class="varname"> flacon</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> flacon</span> est 1 si l'armoire comprend des portes en verre, 0 dans le cas contraire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Nom du iccProfile incorporé dans le <span class="varname"> sourceFile</span>. </p> <p>Vide si <span class="varname"> sourceFile</span> n’est pas géré par couleur. Vignettes seulement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">infos.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Message d’information, tel que des informations de progression. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> est 1 si <span class="varname"> sourceFile</span> est une vignette maître, 0 si elle a déjà été traitée avec <span class="filepath"> vnUpdate</span> ou <span class="filepath"> vntc</span>. Vignettes seulement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> est 0 si <span class="varname"> sourceFile</span> est un style d’armoire contenant des données d’image JPEG (un avertissement est également généré dans ce cas), 1 dans le cas contraire. Fichiers de style d'armoire et de couverture de fenêtre uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Limite de mémoire maximale qui s'applique au processus vntc<span class="filepath"> </span> en cours d'exécution. <span class="varname"> chaîne </span> est <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span> ou <span class="codeph"> 0</span> (désactivé). Où <span class="varname"> K</span>, <span class="varname"> M</span> et <span class="varname"> G</span> font référence aux kilo-octets (1 024 octets), aux méga-octets (1048576 octets) et aux giga-octets (1073741824 octets). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Échelle du niveau de pyramide de résolution le plus bas dans la vignette de sortie. Uniquement présent si <span class="codeph"> -pyramid</span> est spécifié. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de matières enregistrées dans le fichier sourceFile <span class="varname"> </span>. Vignettes seulement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre d’images de panneau dans ce fichier de style armoire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de niveaux de pyramide dans la vignette de sortie. Uniquement présent si -pyramid est spécifié. Vignettes seulement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 si la vignette source ou de destination a une structure pyramidale. Vignettes seulement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">résolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Pour les styles d’armoire, la résolution de l’objet de la <span class="varname"> sourceFile</span>. Pour les vignettes, il s’agit de la résolution de matériau recommandée pour obtenir des résultats de rendu de meilleure qualité lors du rendu de la vignette de sortie. Pixels/pouce (ppp). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Résolution d’objet la plus faible dans la vignette de sortie. Vignettes seulement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Résolution d’objet moyenne dans la vignette de sortie. Vignettes seulement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Chemin d’accès <span class="varname"> sourceFile</span> complet. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Version du fichier <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Taille en pixels de la vignette d’entrée, de l’image de panneau par défaut dans un fichier de style d’armoire ou de la première image d’opacité d’un fichier de style de recouvrement de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Le type de couvre-fenêtre (styles de couvre-fenêtre uniquement) : </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=ombrage horizontal ou stores </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1 = stores verticaux </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=rideaux courts pleine largeur </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=champs courts gauche/droite </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4 = rideaux pleine largeur </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=champs de pleine longueur gauche/droite </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=rideau de café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> si <span class="varname"> sourceFile</span> est une vignette, <span class="codeph"> vnc</span> si <span class="varname"> sourceFile</span> est un style d'armoire, ou <span class="codeph"> vnw</span> si <span class="varname"> sourceFile</span> est un style de recouvrement de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Valeur spécifiée avec <span class="codeph"> -version</span> ou la valeur de <span class="codeph"> defaultFileVersion</span> si <span class="codeph"> -version</span> n’a pas été spécifiée. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Liste séparée par des virgules des tailles en pixels de toutes les vues de la vignette de sortie (vue en pleine résolution pour les vignettes pyramidales), de l’image de panneau par défaut dans un fichier de style d’armoire ou de la première image d’opacité d’un fichier de style de recouvrement de fenêtre. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> est 1 si le style d'armoire est texturable, 0 dans le cas contraire. Non présent pour les fichiers de style de vignettes et de couvre-fenêtres. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">avertissement.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Message d’avertissement (par exemple, lorsque <span class="codeph"> -imagemap</span> est spécifié, mais qu’aucune donnée de mappage n’est trouvée dans la vignette). </p></td> 
 </tr> 
</table>
