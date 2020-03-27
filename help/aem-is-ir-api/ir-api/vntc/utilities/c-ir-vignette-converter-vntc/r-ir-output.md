---
description: vntc génère des données texte envoyées à stderr ou au fichier journal.
seo-description: vntc génère des données texte envoyées à stderr ou au fichier journal.
seo-title: Sortie
solution: Experience Manager
title: Sortie
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Output{#output}

vntc génère des données texte envoyées à stderr ou au fichier journal.

Les données sont formatées sous la forme d’une `name=value` propriété par enregistrement de texte. Les valeurs de chaîne ne sont pas citées. Les messages d’avertissement et d’erreur sont toujours envoyés `stderr`, même si `-log` cela est spécifié.

Certaines propriétés peuvent se produire plusieurs fois dans la même sortie. Un numéro de séquence, commençant par 0, est ajouté au nom de ces propriétés, séparé par un point. Ces propriétés sont identifiées ci-dessous avec un suffixe `. *`n`*` après le nom de la propriété.

Les propriétés suivantes sont générées :

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Couleur d’arrière-plan RVB du style d’armoire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Version du fichier de sortie par défaut. Le numéro de version de fichier le plus élevé que cette version de <span class="filepath"> vntc</span> puisse générer. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">erreur.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Message d’erreur. La présence de messages d’erreur indique généralement qu’aucun fichier de sortie n’est créé ou qu’il ne convient pas à l’utilisation du rendu d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>chemin/nom complet de tous les fichiers de sortie, y compris les vignettes, les fichiers de style d’armoire, les images à résolution intégrale et les images miniatures. Un attribut de fichier est présent pour chaque fichier généré (à l’exception du fichier journal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> est 1 si l'armoire comporte des portes en verre, 0 dans le cas contraire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Nom de l’élément iccProfile incorporé dans le <span class="varname"> fichiersource</span>. </p> <p>Vide si <span class="varname"> sourceFile</span> n’est pas géré par couleur. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Message d’information, tel que les informations de progression. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> est 1 si <span class="varname"> sourceFile</span> est une vignette originale, 0 s’il a été traité précédemment avec <span class="filepath"> vnUpdate</span> ou <span class="filepath"> vntc</span>. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> est égal à 0 si <span class="varname"> sourceFile</span> est un style d’armoire contenant des données d’image JPEG (un avertissement est également généré dans ce cas), 1 dans le cas contraire. Armoire et fenêtre couvrant uniquement les fichiers de style. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Limite de mémoire maximale applicable au processus <span class="filepath"> vntc</span> en cours d'exécution. <span class="varname"> string</span> est soit <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>,  ivalG ou  0(désactivé). <span class="varname"></span><span class="codeph"></span> Où <span class="varname"> K</span>, <span class="varname"> M</span>et <span class="varname"> G</span> font référence aux Ko (1 024 octets), aux Mégaoctets (1 04 8576 octets) et aux Gigaoctets (1 073 74 1 824 octets). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Echelle du niveau de pyramide de la résolution la plus basse dans la vignette de sortie. Uniquement présent si <span class="codeph"> -pyramid</span> est spécifié. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de documents enregistrés dans le <span class="varname"> fichier</span>source. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre d’images de panneau dans ce fichier de style d’armoire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de niveaux de pyramide dans la vignette de sortie. Uniquement présent si -pyramid est spécifié. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 si la vignette source ou de destination possède une structure pyramidale. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Pour les styles d’armoire, résolution d’objet du<span class="varname"> fichiersource</span>. Pour les vignettes, il s’agit de la résolution de matériau recommandée pour obtenir des résultats de rendu de meilleure qualité lors du rendu de la vignette de sortie. Pixels/pouce (ppp). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Plus petite résolution d’objet dans la vignette de sortie. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Résolution moyenne de l’objet dans la vignette de sortie. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Chemin d’accès complet au <span class="varname"> fichier</span> source. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Version de fichier de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Taille en pixels de la vignette d’entrée, de l’image par défaut du panneau dans un fichier de style d’armoire ou de la première image d’opacité d’un fichier de style de recouvrement de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Type de garniture de fenêtre (styles de garniture de fenêtre uniquement) : </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=ombrage ou stores horizontaux </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=stores verticaux </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2 = rideaux courts pleine largeur </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=rideaux courts gauche/droite </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4 = rideaux pleine largeur </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5 = rideaux de pleine longueur gauche/droite </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6 = rideau du café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valeur </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> si <span class="varname"> sourceFile</span> est une vignette, <span class="codeph"> vnc</span> si <span class="varname"> sourceFile</span> est un style d'armoire ou  vnw si  sourceFileest un style de garnissage de fenêtre.<span class="codeph"></span><span class="varname"></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Valeur spécifiée avec <span class="codeph"> -version</span>ou valeur de default<span class="codeph"> FileVersion</span> si<span class="codeph"> -version</span> n’a pas été spécifiée. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSzes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival]</span></span> </p></td> 
  <td class="stentry"> <p>séparé par des virgules, de la taille en pixels de tous les de la vignette de sortie (l’ en résolution maximale pour les vignettes pyramidales), de l’image de panneau par défaut dans un fichier de style d’armoire ou de la première image d’opacité d’un fichier de style de fenêtre. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> est 1 si le style de l'armoire est texturable, 0 dans le cas contraire. Inprésent pour les vignettes et les fichiers de style de garniture de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">avertissement.<span class="varname"> n</span>=<span class="varname"> chaîne</span></span> </p></td> 
  <td class="stentry"> <p>Message d’avertissement (par exemple, lorsque <span class="codeph"> -imagemap</span> est spécifié mais qu’aucune donnée de mappage n’est trouvée dans la vignette). </p></td> 
 </tr> 
</table>

