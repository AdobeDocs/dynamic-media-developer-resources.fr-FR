---
description: vntc génère des données texte qui sont envoyées à stderr ou au fichier journal.
solution: Experience Manager
title: Sortie
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# Sortie{#output}

vntc génère des données texte qui sont envoyées à stderr ou au fichier journal.

Les données sont formatées sous la forme d’une propriété `name=value` par enregistrement texte. Les valeurs de chaîne ne sont pas entre guillemets. Les messages d’avertissement et d’erreur sont toujours envoyés à `stderr`, même si `-log` est spécifié.

Certaines propriétés peuvent se produire plusieurs fois dans la même sortie. Un numéro de séquence, commençant par 0, est ajouté au nom de ces propriétés, séparé par un point. Ces propriétés sont identifiées ci-dessous avec un suffixe `. *`n`*` après le nom de la propriété.

Les propriétés suivantes sont générées :

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>, <span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Couleur d’arrière-plan RVB du style de l’armoire. Styles de cabinet uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Version du fichier de sortie par défaut. Également le numéro de version de fichier le plus élevé que cette version de <span class="filepath"> vntc</span> peut générer. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">erreur.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Message d’erreur. La présence de messages d’erreur indique généralement qu’aucun fichier de sortie n’est créé ou qu’il ne peut pas être utilisé par le rendu d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Chemin/nom complet de tous les fichiers de sortie, y compris les vignettes, les fichiers de style de cabinet, les images à résolution complète et les images miniatures. Un attribut de fichier est présent pour chaque fichier généré (à l’exception du fichier journal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 si l’armoire contient des portes en verre, 0 dans le cas contraire. Styles de cabinet uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Nom du iccProfile incorporé dans le fichier <span class="varname"> sourceFile</span>. </p> <p>Vide si <span class="varname"> sourceFile</span> n’est pas géré par les couleurs. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Message d’information, comme les informations de progression. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 si  <span class="varname"> </span> sourceFileest une vignette maître, 0 s’il a été traité précédemment avec  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span>. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 0 si  <span class="varname"> </span> sourceFileest un style cabinet contenant des données d’image JPEG (un avertissement est également généré dans ce cas), 1 dans le cas contraire. Fichiers de style de garde et de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Limite de mémoire maximale applicable au processus <span class="filepath"> vntc</span> en cours d’exécution. <span class="varname"> </span> chaîne est soit  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> ou  <span class="codeph"> 0</span>  (désactivée). Où <span class="varname"> K</span>, <span class="varname"> M</span> et <span class="varname"> G</span> se rapportent aux kilo-octets (1 024 octets), aux mégaoctets (1048576 octets) et aux gigaoctets (1073741824 octets). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Echelle du niveau de pyramide de résolution le plus bas dans la vignette de sortie. Uniquement présente si <span class="codeph"> -pyramid</span> est spécifié. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMatériaux=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Le nombre de matériaux enregistrés dans le <span class="varname"> sourceFile</span>. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre d’images de panneau dans ce fichier de style Cabinet. Styles de cabinet uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de niveaux pyramidaux dans la vignette de sortie. Uniquement présente si -pyramid est spécifié. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 si la vignette source ou de destination possède une structure pyramidale. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Pour les styles de cabinet, la résolution de l’objet du <span class="varname"> sourceFile</span>. Pour les vignettes, il s’agit de la résolution matérielle recommandée pour des résultats de rendu de meilleure qualité lors du rendu de la vignette de sortie. Pixels/pouces (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Résolution d’objet la plus petite de la vignette de sortie. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Résolution d’objet moyenne dans la vignette de sortie. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Chemin d’accès complet <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Version du fichier de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Taille en pixels de la vignette d’entrée, de l’image de panneau par défaut dans un fichier de style d’armoire ou de la première image d’opacité d’une fenêtre recouvrant un fichier de style. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Le type de recouvrement de fenêtre (styles de recouvrement de fenêtre uniquement) : </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0 = nuance horizontale ou stores </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1 = stores verticaux </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2 = rideaux courts pleine largeur </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3 = rideaux courts gauche/droite </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4 = rideaux pleine largeur </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5 = rideaux de plein pied gauche/droite </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6 = rideau du café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valeur </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileest une vignette,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFileis est un style Cabinet ou  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFileest une fenêtre qui couvre le style. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La valeur spécifiée avec <span class="codeph"> -version</span> ou la valeur de<span class="codeph"> defaultFileVersion</span> si<span class="codeph"> -version</span> n’a pas été spécifiée. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSzes=<span class="varname"> ival</span>, <span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Liste séparée par des virgules des tailles de pixels de toutes les vues dans la vignette de sortie (l’affichage en pleine résolution des vignettes pyramidales), de l’image de panneau par défaut dans un fichier de style Cabinet ou de la première image d’opacité d’une fenêtre recouvrant un fichier de style. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 si le style de l’armoire est texturable, 0 dans le cas contraire. Non présent pour les fichiers de style de vignettes et de recouvrements de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">avertissement.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Message d’avertissement (par exemple, lorsque <span class="codeph"> -imagemap</span> est spécifié mais qu’aucune donnée de carte n’est trouvée dans la vignette). </p></td> 
 </tr> 
</table>
