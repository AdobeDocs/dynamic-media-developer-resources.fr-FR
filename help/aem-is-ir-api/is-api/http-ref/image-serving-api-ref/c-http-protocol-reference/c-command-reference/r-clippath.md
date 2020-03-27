---
description: Chemin du clip de calque Spécifie un chemin d’accès à l’élément pour le calque actif.
seo-description: Chemin du clip de calque Spécifie un chemin d’accès à l’élément pour le calque actif.
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipPath{#clippath}

Chemin du clip de calque Spécifie un chemin d’accès à l’élément pour le calque actif.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cheminNom</span></span> </p> </td> 
  <td class="stentry"> <p>Nom du chemin d’accès incorporé dans l’image source du calque (ASCII uniquement). </p></td> 
 </tr> 
</table>

Toutes les parties du calque situées en dehors de la zone définie par `clipPath=` sont rendues transparentes.

` *`pathName`*` est le nom d’un chemin incorporé dans l’image source du calque. Le chemin est automatiquement transformé afin de conserver un alignement relatif avec le contenu de l’image. Si plusieurs ` *`cheminsName`*` sont spécifiés, le serveur cliente l’image à l’intersection de ces chemins. Tout ` *`cheminName`*` introuvable dans l’image source est ignoré.

>[!NOTE]
>
>Seules les chaînes ASCII sont prises en charge pour ` *`pathName`*`.

` *`pathDefinition`*` permet de spécifier des données de chemin explicites dans les coordonnées de pixels du calque.

Si `size=` est spécifié et non pas 0,0, le calque est prédimensionné. Dans ce cas, les coordonnées du chemin sont relatives au coin supérieur gauche du rectangle du calque et le calque est positionné selon `origin=` ou selon sa valeur par défaut. Toutes les zones du chemin en dehors du rectangle du calque restent transparentes.

Si `size=` il n’est pas spécifié pour une couleur unie ou un calque de texte, le calque est considéré comme auto-dimensionné, l’étendue du chemin déterminant sa taille. Si `origin=` ce paramètre n’est pas spécifié, il prend par défaut la valeur (0,0) de l’espace de coordonnées du chemin. Cela permet effectivement de spécifier les coordonnées du chemin par rapport au   de la couche 0.

>[!NOTE]
>
>`scale=`, `rotate=`et `anchor=` les commandes ne sont pas autorisées pour le redimensionnement automatique des calques de couleur unie.

` *`pathDefinition`*` accepte une chaîne similaire à la valeur de l’ `d=` attribut de l’ `<path>` élément SVG, sauf que des virgules sont utilisées à la place d’espaces pour séparer les valeurs. ` *`pathDefinition`*` peut inclure un ou plusieurs sous-chemins de boucle fermée.

Les commandes de chemin suivantes sont prises en charge dans ` *`pathDefinition`*`:

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Commande</b> </th> 
   <th class="entry"> <b> Nom</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> moveto absolu </p> </td> 
   <td> <p> d’un nouveau sous-chemin à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> moveto </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolu </p> </td> 
   <td> <p> Tracez une ligne de la position actuelle à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relatif </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absolu </p> </td> 
   <td> <p> Tracez une courbe de Bézier de la position actuelle à x,y. x1,y1 est le point de contrôle au début de la courbe et x2,y2 est le point de contrôle à la fin de la courbe. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relatif </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Fermez le sous-chemin actuel avec une ligne droite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les commandes en majuscules indiquent que les valeurs des coordonnées se situent à des positions en pixels absolus (par rapport au coin supérieur gauche du rectangle du calque). Les décalages de pixels suivent les commandes en minuscules par rapport à la position actuelle.

&#39;m&#39; ou &#39;M&#39;  toujours un nouveau sous-chemin. Les sous-chemins sont fermés automatiquement (avec une ligne droite) si &#39;Z&#39; ou &#39;z&#39; n&#39;est pas spécifié à la fin.

Si un sous-chemin commence par un moveto relatif (&#39;m&#39;), il est relatif à l&#39;un des éléments suivants :

* Point de départ du sous-chemin précédent, s’il était fermé avec &#39;z&#39; ou &#39;Z&#39;.
* Point de fin du sous-chemin précédent, s’il n’était pas fermé explicitement.
* 0,0, s’il s’agit du premier sous-chemin.

## Propriétés {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attribut de calque. S’applique au calque actif ou à l’image composite, le cas échéant `layer=comp`. Les calques d’effets l’ignorent.

`clipPathE=` est ignorée si aucun chemin d’accès portant le nom spécifié n’est trouvé dans l’image source du calque ou si la source du calque n’est pas une image.

## Par défaut {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Aucun, pour aucun autre écrêtage du calque.

## Voir aussi {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
