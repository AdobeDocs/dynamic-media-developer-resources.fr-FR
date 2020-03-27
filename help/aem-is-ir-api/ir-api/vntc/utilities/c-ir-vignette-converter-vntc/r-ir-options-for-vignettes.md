---
description: Les options suivantes contrôlent le traitement des fichiers de vignettes. Elles sont ignorées si sourceFile n’est pas une vignette.
seo-description: Les options suivantes contrôlent le traitement des fichiers de vignettes. Elles sont ignorées si sourceFile n’est pas une vignette.
seo-title: Options pour les vignettes
solution: Experience Manager
title: Options pour les vignettes
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Options pour les vignettes{#options-for-vignettes}

Les options suivantes contrôlent le traitement des fichiers de vignettes. Elles sont ignorées si sourceFile n’est pas une vignette.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contenu</span> </p></td> 
  <td class="stentry"> <p>Crée un fichier XML représentant la hiérarchie d’objets et incluant les attributs d’objet sélectionnés. Le contenu du fichier est identique à celui renvoyé par la commande <span class="codeph"> req=contents</span> . Le fichier porte le même nom que le fichier source, mais avec un suffixe <span class="filepath"> .xml</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-recadrer <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> avec</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> est le coin supérieur gauche du rectangle de recadrage et <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> est la taille du rectangle de recadrage. Les valeurs sont des coordonnées de pixels par rapport à l’image de  de la vignette source en résolution maximale. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn hein</span><span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>Recadrez la vignette avant de la mettre à l’échelle. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> est le coin supérieur gauche du rectangle de recadrage, et widn <span class="codeph"><span class="varname"> ,</span>hein<span class="varname"></span></span> est la taille du rectangle de recadrage. Les valeurs sont normalisées par rapport à l’image  du vignette source et doivent être comprises entre 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> et <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> ne doivent pas dépasser 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -matériaux d'intégration</span> </p></td> 
  <td class="stentry"> <p>Conservez les matériaux incorporés dans la vignette de sortie. Par défaut, les matériaux sont supprimés de la vignette de sortie. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs vignettes de sortie sont en hauteur en pixels. Ignoré si -info est spécifié. <span class="varname"> ival</span> peut être 0, ce qui indique la largeur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle</a> de la vignette pour plus d’informations. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Activez   du fichier de zone cliquable à partir de la vignette. Les données de mappage sont écrites dans un fichier HTML contenant uniquement un <span class="codeph"> élément &lt;map&gt;</span> . Le fichier de sortie est nommé de la même manière que le fichier image de sortie, mais avec un suffixe <span class="filepath"> .htm</span> . Un message d’avertissement est généré et aucun fichier n’est créé si la commande est spécifiée mais qu’aucune donnée de mappage n’est présente dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profil</span> </p></td> 
  <td class="stentry"> <p>Enregistre une copie du ICC  incorporé dans la vignette dans un fichier. Un message d’avertissement est généré et aucun fichier  ICC n’est créé si la commande est spécifiée mais qu’aucun ICC n’est présent dans la vignette. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pyramide</span> </p></td> 
  <td class="stentry"> <p>Crée une vignette pyramidale. Obligatoire lorsque les images rendues doivent être affichées avec les visionneuses de zoom Scene7. Voir Mise à l’échelle <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> de</a> la vignette pour plus d’informations. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Contrainte de largeur et de hauteur des pixels pour l’image miniature. Si elle est spécifiée, une image JPEG qui n’est pas plus large et pas plus grande que <span class="varname"> la valeur ivoirienne</span> est générée à partir de l’image  vignette, d’une image de panneau du fichier de style d’armoire ou de la carte d’éclairage du premier style du fichier de style de garnitures de fenêtre. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Une ou plusieurs largeurs de vignette de sortie en pixels. Ignoré si <span class="codeph"> -info</span> est spécifié. <span class="varname"> ival</span> peut être 0, ce qui indique la hauteur de la vignette d’entrée. Voir <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Mise à l’échelle</a> de la vignette pour plus d’informations. </p></td> 
 </tr> 
</table>

