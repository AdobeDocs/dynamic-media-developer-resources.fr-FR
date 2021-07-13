---
description: Les options suivantes contrôlent le traitement des fichiers de vignettes. Ils sont ignorés si sourceFile n’est pas une vignette.
solution: Experience Manager
title: Options des vignettes
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Options des vignettes{#options-for-vignettes}

Les options suivantes contrôlent le traitement des fichiers de vignettes. Ils sont ignorés si sourceFile n’est pas une vignette.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contenu</span> </p></td> 
  <td class="stentry"> <p>Crée un fichier XML représentant la hiérarchie d’objets et incluant les attributs d’objets sélectionnés. Le contenu du fichier est le même que celui renvoyé par la commande <span class="codeph"> req=contents</span> . Le fichier porte le même nom que le fichier source, mais avec un suffixe <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> x</span>, <span class="varname"> </span></span> correspond au coin supérieur gauche du rectangle de recadrage, et  <span class="codeph"><span class="varname"> avec</span>, <span class="varname"> </span></span>  correspond à la taille du rectangle de recadrage. Les valeurs sont des coordonnées en pixels par rapport à l’image en résolution complète de la vignette source. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> xn</span>, <span class="varname"> </span></span> correspond au coin supérieur gauche du rectangle de recadrage, et  <span class="codeph"><span class="varname"> large</span>, <span class="varname"> </span></span> correspond à la taille du rectangle de recadrage. Les valeurs sont normalisées par rapport à l’image de la vignette source et doivent être comprises entre 0,0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> width et  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinin ne doivent pas être supérieures à 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -embedded matériaux</span> </p></td> 
  <td class="stentry"> <p>Conserver les matériaux incorporés dans la vignette de sortie. Par défaut, les matériaux sont supprimés de la vignette de sortie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs vignettes de sortie sont hautes en pixels. Ignoré si -info est spécifié. <span class="varname"> </span> ivalpeut être 0, ce qui indique la largeur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle de la vignette</a> pour plus d’informations. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Activez l’extraction du fichier de zone cliquable à partir de la vignette. Les données de mappage sont écrites dans un fichier HTML contenant uniquement un élément <span class="codeph"> &lt;map&gt;</span> . Le fichier de sortie est nommé de la même manière que le fichier image de sortie, mais avec un suffixe <span class="filepath"> .htm</span>. Un message d’avertissement est généré et aucun fichier n’est créé si la commande est spécifiée, mais qu’aucune donnée map n’est présente dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profil</span> </p></td> 
  <td class="stentry"> <p>Enregistre dans un fichier une copie du profil ICC incorporé dans la vignette. Un message d’avertissement est généré et aucun fichier de profil ICC n’est créé si la commande est spécifiée mais qu’aucun profil ICC n’est présent dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramid</span> </p></td> 
  <td class="stentry"> <p>Crée une vignette pyramidale. Obligatoire lors de l’affichage des images rendues avec les visionneuses de zoom Dynamic Media. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle de la vignette</a> pour plus d’informations. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Contrainte de largeur et de hauteur en pixels pour l’image miniature. Si cette valeur est spécifiée, une image JPEG qui n’est pas plus grande et pas plus grande que <span class="varname"> ival</span> est générée à partir de l’image d’affichage de la vignette, d’une image de panneau du fichier de style de l’armoire ou de la carte d’éclairage du premier style du fichier de style de recouvrements de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs largeurs de vignette de sortie en pixels. Ignoré si <span class="codeph"> -info</span> est spécifié. <span class="varname"> </span> ivalpeut être 0, ce qui indique la hauteur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle de la vignette</a> pour plus d’informations. </p></td> 
 </tr> 
</table>
