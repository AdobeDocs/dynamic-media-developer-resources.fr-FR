---
description: Les options suivantes contrôlent le traitement des fichiers de vignettes. Ils sont ignorés si sourceFile n’est pas une vignette.
solution: Experience Manager
title: Options pour les vignettes
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# Options pour les vignettes{#options-for-vignettes}

Les options suivantes contrôlent le traitement des fichiers de vignettes. Ils sont ignorés si sourceFile n’est pas une vignette.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contenu</span> </p></td> 
  <td class="stentry"> <p>Crée un fichier XML représentant la hiérarchie d’objets et incluant les attributs d’objet sélectionnés. Le contenu du fichier est identique à celui renvoyé par la commande <span class="codeph"> req=contents</span>. Le fichier porte le même nom que le fichier source, mais avec le suffixe <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-recadrer  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywiwihei</span></span> </p></td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> </span></span> c’est le coin supérieur gauche du rectangle de recadrage et,  <span class="codeph"><span class="varname"> avec</span>,<span class="varname"> </span></span> il correspond à la taille du rectangle de recadrage. Les valeurs sont des coordonnées en pixels par rapport à l’image de vue de résolution complète de la vignette source. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwinhein</span></span> </p> </td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> ynis le coin supérieur gauche du rectangle de recadrage, et  <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> </span></span> heinis la taille du rectangle de recadrage. Les valeurs sont normalisées par rapport à l’image de vue de la vignette source et doivent être comprises entre 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> width et  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> heinand ne doivent pas dépasser 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -matériaux d'intégration</span> </p></td> 
  <td class="stentry"> <p>Conservez les matériaux incorporés dans la vignette de sortie. Par défaut, les matériaux sont supprimés de la vignette de sortie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs vignettes de sortie ont une hauteur en pixels. Ignoré si -info est spécifié. <span class="varname"> </span> ivalpeut être 0, ce qui indique la largeur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle des vignettes</a> pour obtenir des informations détaillées. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Activez l’extraction du fichier de zone cliquable à partir de la vignette. Les données de mappage sont écrites dans un fichier HTML contenant uniquement un élément <span class="codeph"> &lt;map&gt;</span>. Le fichier de sortie est nommé de la même manière que le fichier d’image de sortie, mais avec un suffixe <span class="filepath"> .htm</span>. Un message d’avertissement est généré et aucun fichier n’est créé si la commande est spécifiée mais qu’aucune donnée de mappage n’est présente dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profil</span> </p></td> 
  <td class="stentry"> <p>Enregistre dans un fichier une copie du profil ICC incorporé dans la vignette. Un message d’avertissement est généré et aucun fichier de profil ICC n’est créé si la commande est spécifiée mais qu’aucun profil ICC n’est présent dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramide</span> </p></td> 
  <td class="stentry"> <p>Crée une vignette pyramidale. Obligatoire lorsque les images rendues doivent être affichées avec les visionneuses de zoom Dynamic Media. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle des vignettes</a> pour plus d’informations. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Contrainte de largeur et de hauteur en pixels pour l’image miniature. Si elle est spécifiée, une image JPEG qui n’est pas plus large et pas plus grande que <span class="varname"> ival</span> est générée à partir de l’image de la vue de vignettes, d’une image de panneau du fichier de style d’armoire ou de la carte d’éclairage du premier style du fichier de style de garnitures de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs largeurs de vignette de sortie en pixels. Ignoré si <span class="codeph"> -info</span> est spécifié. <span class="varname"> </span> ivalpeut être 0, ce qui indique la hauteur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle des vignettes</a> pour obtenir des informations détaillées. </p></td> 
 </tr> 
</table>

