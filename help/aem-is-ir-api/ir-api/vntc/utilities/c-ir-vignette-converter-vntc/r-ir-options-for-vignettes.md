---
description: Les options suivantes contrôlent le traitement des fichiers de vignette. Elles sont ignorées si sourceFile n’est pas une vignette.
solution: Experience Manager
title: Options des vignettes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Options des vignettes{#options-for-vignettes}

Les options suivantes contrôlent le traitement des fichiers de vignette. Elles sont ignorées si sourceFile n’est pas une vignette.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>Crée un fichier XML représentant la hiérarchie de l’objet et incluant les attributs d’objet sélectionnés. Le contenu du fichier est identique à celui renvoyé par la commande <span class="codeph"> req=contents</span>. Le fichier porte le même nom que le fichier source, mais avec un suffixe .xml<span class="filepath"> </span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> recadrage <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> est le coin supérieur gauche du rectangle de recadrage et <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> est la taille du rectangle de recadrage. Les valeurs sont des coordonnées en pixels par rapport à l’image d’affichage en pleine résolution de la vignette source. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> est le coin supérieur gauche du rectangle de recadrage, et <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> est la taille du rectangle de recadrage. Les valeurs sont normalisées par rapport à l'image de la vignette source et doivent être comprises entre 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> et <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> ne doivent pas dépasser 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -matériaux incorporés</span> </p></td> 
  <td class="stentry"> <p>Conserver les matériaux incorporés dans la vignette de sortie. Par défaut, les matériaux sont supprimés de la vignette de sortie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-hauteur <span class="varname"> flacon </span></span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs hauteurs de vignette de sortie en pixels. Ignoré si -info est spécifié. <span class="varname"> ival</span> peut être 0, ce qui indique la largeur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> pour plus d’informations. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Activez l’extraction du fichier de zone cliquable de la vignette. Les données de mappage sont écrites dans un fichier HTML contenant uniquement un élément <span class="codeph"> &lt;map&gt;</span>. Le nom du fichier de sortie est identique à celui du fichier image de sortie, mais avec un suffixe <span class="filepath"> .htm</span>. Un message d'avertissement est généré et aucun fichier n'est créé si la commande est spécifiée mais qu'aucune donnée map n'est présente dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Enregistre une copie du profil ICC incorporé dans la vignette dans un fichier. Un message d'avertissement est généré et aucun fichier de profil ICC n'est créé si la commande est spécifiée mais qu'aucun profil ICC n'est présent dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramide</span> </p></td> 
  <td class="stentry"> <p>Crée une vignette pyramidale. Obligatoire lorsque les images rendues doivent être affichées avec les visionneuses de zoom Dynamic Media. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> pour plus d'informations. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Contrainte de largeur et de hauteur en pixels pour l’image miniature. Si elle est spécifiée, une image JPEG dont la largeur et la hauteur ne dépassent pas <span class="varname"> ival</span> est générée à partir de l'image de la vue vignette, d'une image de panneau du fichier de style d'armoire ou de la carte d'illumination du premier style dans le fichier de style des couvre-fenêtres. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs largeurs de vignette de sortie en pixels. Ignoré si <span class="codeph"> -info</span> est spécifié. <span class="varname"> ival</span> peut être 0, ce qui indique la hauteur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Vignette Scaling</a> pour plus d’informations. </p></td> 
 </tr> 
</table>
