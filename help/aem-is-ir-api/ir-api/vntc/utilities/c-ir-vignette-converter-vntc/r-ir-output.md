---
description: vntc génère des données texte envoyées à stderr ou au fichier journal.
solution: Experience Manager
title: Sortie
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 0%

---


# Output{#output}

vntc génère des données texte envoyées à stderr ou au fichier journal.

Les données sont formatées sous la forme d’une propriété `name=value` par enregistrement de texte. Les valeurs de chaîne ne sont pas citées. Les messages d&#39;avertissement et d&#39;erreur sont toujours envoyés à `stderr`, même si `-log` est spécifié.

Certaines propriétés peuvent se produire plusieurs fois dans la même sortie. Un numéro de séquence, commençant par 0, est ajouté au nom de ces propriétés, séparé par un point. Ces propriétés sont identifiées ci-dessous avec un suffixe `. *`n`*` après le nom de la propriété.

Les propriétés suivantes sont générées :

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>Couleur d’arrière-plan RVB du style d’armoire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Version du fichier de sortie par défaut. Le numéro de version de fichier le plus élevé que cette version de <span class="filepath"> vntc</span> peut générer. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">erreur.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Message d’erreur. La présence de messages d’erreur indique généralement qu’aucun fichier de sortie n’est créé ou qu’il ne peut pas être utilisé par le rendu d’image. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>chemin d’accès complet/nom de tous les fichiers de sortie, y compris les vignettes, les fichiers de style d’armoire, les images à résolution totale et les images miniatures. Un attribut de fichier est présent pour chaque fichier généré (à l’exception du fichier journal). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 si l'armoire comporte des portes en verre, 0 autrement. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Nom de l’élément iccProfile incorporé dans le <span class="varname"> sourceFile</span>. </p> <p>Vide si <span class="varname"> sourceFile</span> n’est pas géré par couleur. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Message d’information, tel que les informations d’avancement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 si  <span class="varname"> </span> sourceFileest une vignette maître, 0 si elle a été traitée précédemment avec  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span>. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 0 si  <span class="varname"> </span> sourceFileest un style d’armoire contenant des données d’image JPEG (un avertissement est également généré dans ce cas), 1 dans le cas contraire. Armoire et fenêtre couvrant uniquement les fichiers de style. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Limite de mémoire maximale applicable au processus en cours d'exécution <span class="filepath"> vntc</span>. <span class="varname"> </span> chaîne est soit  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>, ivalG, ou bien 0(désactivé).<span class="varname"></span><span class="codeph"></span> Où <span class="varname"> K</span>, <span class="varname"> M</span> et <span class="varname"> G</span> se rapportent à des kilooctets (1 024 octets), des mégaoctets (1 048 576 octets) et des gigaoctets (1 073 74182 4 octets). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Échelle de la pyramide de résolution la plus basse dans la vignette de sortie. Uniquement présent si <span class="codeph"> -pyramid</span> est spécifié. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de matériaux enregistrés dans le fichier source <span class="varname"> </span>. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre d'images de panneau dans ce fichier de style d'armoire. Styles d’armoire uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Nombre de niveaux pyramidaux dans la vignette de sortie. Uniquement présent si -pyramid est spécifié. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 si la vignette source ou de destination possède une structure pyramidale. Vignettes uniquement. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Pour les styles d'armoire, résolution d'objet du fichier source<span class="varname"> sourceFile</span>. Pour les vignettes, il s’agit de la résolution de matériau recommandée pour obtenir des résultats de rendu de meilleure qualité lors du rendu de la vignette de sortie. Pixels/pouce (ppp). </p></td> 
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
  <td class="stentry"> <p>Version de fichier de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Taille en pixels de la vignette d’entrée, de l’image de panneau par défaut dans un fichier de style d’armoire ou de la première image d’opacité d’une fenêtre recouvrant un fichier de style. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Type de recouvrement de fenêtre (style de recouvrement de fenêtre uniquement) : </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=ombrage ou stores horizontaux </li> 
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
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileis est une vignette,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFileis est un style d'armoire, ou  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFileis est un style de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>La valeur spécifiée avec <span class="codeph"> -version</span> ou la valeur de <span class="codeph"> defaultFileVersion</span> si <span class="codeph"> -version</span> n'a pas été spécifiée. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSzes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival]</span></span> </p></td> 
  <td class="stentry"> <p>Liste séparée par des virgules des tailles de pixels de toutes les vues de la vignette de sortie (la vue de résolution complète pour les vignettes pyramidales), de l’image de panneau par défaut dans un fichier de style d’armoire ou de la première image d’opacité d’une fenêtre couvrant le fichier de style. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 si le style de l'armoire est texturable, 0 sinon. Indisponible pour les fichiers de style de vignettes et de garnitures de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">avertissement.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Message d’avertissement (par exemple, lorsque <span class="codeph"> -imagemap</span> est spécifié mais qu’aucune donnée de mappage n’est trouvée dans la vignette). </p></td> 
 </tr> 
</table>

