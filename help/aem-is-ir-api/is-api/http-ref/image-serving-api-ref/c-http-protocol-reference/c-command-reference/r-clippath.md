---
title: clipPath
description: Chemin d’accès au clip de calque. Spécifie un chemin d’accès à l’élément pour le calque actif.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# clipPath{#clippath}

Chemin d’accès au clip de calque. Spécifie un chemin d’accès à l’élément pour le calque actif.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>Données de chemin d’accès. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nom du chemin d’accès incorporé dans l’image source du calque (ASCII uniquement). </p></td> 
 </tr> 
</table>

Toutes les parties du calque situées en dehors de la zone définie par `clipPath=` sont rendues transparentes.

`*`pathName`*` est le nom d’un chemin incorporé dans l’image source du calque. Le chemin est automatiquement transformé afin de conserver un alignement relatif avec le contenu de l’image. Si plusieurs `*`pathName`*` sont spécifiés, le serveur cliente l’image à l’intersection de ces chemins. Tout `*`pathName`*` introuvable dans l’image source est ignoré.

>[!NOTE]
>
>Seules les chaînes ASCII sont prises en charge pour `*`pathName`*`.

`*`pathDefinition`*` permet de spécifier des données de chemin d’accès explicites dans les coordonnées des pixels de couche.

Si `size=` est spécifié et non 0,0, le calque est prédimensionné. Dans ce cas, les coordonnées du chemin sont relatives au coin supérieur gauche du rectangle du calque et le calque est positionné sur la base de `origin=` ou de sa valeur par défaut. Toutes les zones du chemin en dehors du rectangle du calque restent transparentes.

Si `size=` n’est pas spécifié pour une couleur ou un calque de texte uni, le calque est considéré comme auto-dimensionnant, l’étendue du chemin déterminant sa taille. Si `origin=` n’est pas spécifié, l’espace de coordonnées du chemin est défini par défaut sur (0,0). Ce processus de workflow permet de spécifier les coordonnées du chemin par rapport à l’origine de la couche 0.

>[!NOTE]
>
>Les commandes `scale=`, `rotate=` et `anchor=` ne sont pas autorisées pour l’auto-dimensionnement des calques de couleur unis.

`*`pathDefinition`*` accepte une chaîne similaire à la valeur de l’attribut `d=` de l’élément `<path>` du SVG, sauf que les virgules sont utilisées à la place d’espaces pour séparer les valeurs. `*`pathDefinition`*` peut inclure un ou plusieurs sous-chemins de boucle fermée.

Les commandes de chemin d’accès suivantes sont prises en charge dans `*`pathDefinition`*` :

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Commande</b> </th> 
   <th class="entry"> <b> Name</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> moveto absolute </p> </td> 
   <td> <p> Démarrez un nouveau sous-chemin à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> moveto relatif </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolute </p> </td> 
   <td> <p> Tracez une ligne de la position actuelle à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *&lbrace;<span class="varname"> x1,y1,x2,y2,x,y</span> </td> 
   <td> <p> curveto absolute </p> </td> 
   <td> <p> Tracez une courbe Bézier de la position actuelle à x,y. x1,y1 est le point de contrôle au début de la courbe et x2,y2 est le point de contrôle à la fin de la courbe. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *&lbrace;<span class="varname"> x1,y1,x2,y2,x,y</span> </td> 
   <td> <p> curveto relatif </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> Fermez le sous-chemin actuel avec une ligne droite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les commandes en majuscules indiquent que les valeurs des coordonnées se situent à des positions en pixels absolues (par rapport au coin supérieur gauche du rectangle du calque). Les décalages de pixels suivent des commandes en minuscules par rapport à la position actuelle.

&#39;m&#39; ou &#39;M&#39; commence toujours un nouveau sous-chemin. Les sous-chemins sont fermés automatiquement (avec une ligne droite) si &quot;Z&quot; ou &quot;z&quot; n’est pas spécifié à la fin.

Si un sous-chemin commence par un mouvement relatif (&#39;m&#39;), il est relatif à l’un des éléments suivants :

* Le point de départ du sous-chemin précédent, s’il a été fermé avec &quot;z&quot; ou &quot;Z&quot;.
* Point de fin du sous-chemin précédent, s’il n’a pas été fermé explicitement.
* 0,0, s’il s’agit du premier sous-chemin.

## Propriétés {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attribut de calque. S’applique au calque actif ou à l’image composite si `layer=comp`. Les calques d’effet l’ignorent.

Le modificateur `clipPathE=` est ignoré si aucun chemin d’accès portant le nom spécifié n’est trouvé dans l’image source du calque ou si la source du calque n’est pas une image.

## Par défaut {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Aucun, pour aucun autre écrêtage du calque.

## Voir aussi {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extension=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
