---
description: Chemin d’accès de l’élément de calque Spécifie un chemin d’accès à l’élément pour le calque actif.
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '552'
ht-degree: 1%

---


# clipPath{#clippath}

Chemin d’accès de l’élément de calque Spécifie un chemin d’accès à l’élément pour le calque actif.

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Path data. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nom du chemin d’accès incorporé à l’image source du calque (ASCII uniquement). </p></td> 
 </tr> 
</table>

Toutes les parties du calque situées en dehors de la zone définie par `clipPath=` sont rendues transparentes.

`*``*` pathName est le nom d’un chemin incorporé à l’image source du calque. Le chemin est automatiquement transformé pour conserver un alignement relatif avec le contenu de l’image. Si plusieurs `*`pathName`*` sont spécifiés, le serveur cliente l’image à l’intersection de ces chemins d’accès. Tout `*`cheminName`*` introuvable dans l&#39;image source est ignoré.

>[!NOTE]
>
>Seules les chaînes ASCII sont prises en charge pour `*`pathName`*`.

`*``*` pathDefinitionpermet de spécifier des données de chemin explicites dans les coordonnées de pixels de calque.

Si `size=` est spécifié et non 0,0, le calque est prédimensionné. Dans ce cas, les coordonnées de chemin sont relatives au coin supérieur gauche du rectangle du calque et le calque est positionné selon `origin=` ou sa valeur par défaut. Toutes les zones du chemin en dehors du rectangle du calque restent transparentes.

Si `size=` n’est pas spécifié pour une couleur unie ou un calque de texte, le calque est considéré comme auto-dimensionné, l’étendue du chemin déterminant sa taille. Si `origin=` n&#39;est pas spécifié, il prend par défaut (0,0) pour l&#39;espace de coordonnées du chemin. Cela permet de spécifier les coordonnées du chemin par rapport à l&#39;origine de la couche 0.

>[!NOTE]
>
>`scale=`,  `rotate=` et  `anchor=` les commandes ne sont pas autorisées pour les calques de couleur unie auto-dimensionnés.

`*``*` pathDefinition accepte une chaîne similaire à la valeur de l’ `d=` attribut de l’ `<path>` élément SVG, sauf que des virgules sont utilisées à la place d’espaces pour séparer les valeurs. `*``*` pathDefinition peut inclure un ou plusieurs sous-chemins en boucle fermée.

Les commandes de chemin suivantes sont prises en charge dans `*`pathDefinition`*` :

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
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> absolu </p> </td> 
   <td> <p> Début d’un nouveau sous-chemin à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> relatif </p> </td> 
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
   <td> <p> Tracez une courbe de Bézier de la position actuelle à x,y. x1,y1 est le point de contrôle au début de la courbe et x2,y2 le point de contrôle à la fin de la courbe. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto relatif </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Fermez le sous-chemin actuel avec une ligne droite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les commandes en majuscules indiquent que les valeurs de coordonnées se trouvent à des positions en pixels absolus (par rapport au coin supérieur gauche du rectangle du calque). Les décalages de pixels suivent les commandes en minuscules par rapport à la position actuelle.

&#39;m&#39; ou &#39;M&#39; début toujours un nouveau sous-chemin. Les sous-chemins sont fermés automatiquement (avec une ligne droite) si &#39;Z&#39; ou &#39;z&#39; n&#39;est pas spécifié à la fin.

Si un sous-chemin commence par un moveto relatif (&#39;m&#39;), il est relatif à l&#39;un des éléments suivants :

* Point de départ du sous-chemin précédent, s&#39;il a été fermé avec &#39;z&#39; ou &#39;Z&#39;.
* Point de terminaison du sous-chemin précédent, s’il n’a pas été fermé explicitement.
* 0,0, s’il s’agit du premier sous-chemin.

## Propriétés {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attribut de couche. S’applique au calque actif ou à l’image composite si `layer=comp`. Les calques d’effets l’ignorent.

`clipPathE=` est ignoré si aucun chemin d’accès portant le nom spécifié n’est trouvé dans l’image source du calque ou si la source du calque n’est pas une image.

## Par défaut {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Aucun, pour qu’aucun autre écrêtage du calque ne soit effectué.

## Voir aussi {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extended=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
