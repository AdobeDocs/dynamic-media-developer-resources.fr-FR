---
title: Chemin d’accès
description: Chemin d’Clip calque. Spécifie un chemin de tracé pour le calque actif.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# Chemin d’accès{#clippath}

Chemin d’Clip calque. Spécifie un chemin de tracé pour le calque actif.

`clipPath= *`Définition du chemin`*`

`clipPathE= *`Nom du chemin`*&#42;[, *`Nom du chemin`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Définition du</span> chemin </span> </p> </td> 
  <td class="stentry"> <p>Données de chemin. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> Chemin</span></span> </p> </td> 
  <td class="stentry"> <p>Nom du chemin incorporé dans l’image source du calque (ASCII uniquement). </p></td> 
 </tr> 
</table>

Toutes les parties du calque situées en dehors de la zone définie par `clipPath=` sont rendues transparentes.

`*`pathName`*` est le nom d’un chemin incorporé dans l’image source du calque. Le chemin est automatiquement transformé pour conserver un alignement relatif avec le contenu de l’image. Si plusieurs `*`pathName`*` sont spécifiés, le serveur découpe l’image à l’intersection de ces chemins. Tout `*`Nom de chemin`*` introuvable dans l’image source est ignoré.

>[!NOTE]
>
>Seules les chaînes ASCII sont prises en charge pour `*`pathName`*`.

`*`pathDefinition`*` permet de spécifier des données de chemin explicites dans les coordonnées des pixels de calque.

Si `size=` est spécifié et non 0,0, le calque est prédimensionné. Dans ce cas, les coordonnées de chemin sont relatives au coin supérieur gauche du rectangle de calque et le calque est positionné en `origin=` fonction de sa valeur par défaut. Toutes les parties du tracé situées à l’extérieur du rectangle du calque restent transparentes.

Si `size=` n’est pas spécifié pour un calque de couleur unie ou de texte, le calque est considéré comme auto-dimensionné, l’étendue du chemin déterminant sa taille. Si `origin=` n’est pas spécifié, elle prend par défaut (0,0) de l’espace de coordonnées du chemin. Ce processus de flux de travail permet effectivement de spécifier les coordonnées de chemin par rapport à l’origine du calque 0.

>[!NOTE]
>
>`scale=`, `rotate=`et `anchor=` les commandes ne sont pas autorisées pour les calques de couleur unie auto-dimensionnants.

`*`pathDefinition`*` accepte une chaîne similaire à la valeur de l’attribut de l’élément `d=` SVG `<path>` , sauf que des virgules sont utilisées à la place d’espaces pour séparer les valeurs. `*`pathDefinition`*` peut inclure un ou plusieurs sous-chemins en boucle fermée.

Les commandes de chemin suivantes sont prises en charge dans `*`pathDefinition`*` :

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Commander</b> </th> 
   <th class="entry"> <b> Nom</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> Déplacer vers l’absolu </p> </td> 
   <td> <p> Démarrez un nouveau sous-chemin à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,Y</span> </td> 
   <td> <p> Déplacer vers le relatif </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b></b> L *{<span class="varname"> x,y</span>} </td> 
   <td> <p> Linéaire absolu </p> </td> 
   <td> <p> Draw une ligne de la position actuelle à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b></b> l *{<span class="varname"> x,y</span>} </td> 
   <td> <p> Relative à la ligne </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> de la courbe à l’absolu </p> </td> 
   <td> <p> Draw une courbe de Bézier de la position actuelle à x,y. x1,y1 est le point de contrôle au début de la courbe et x2,y2 est le point de contrôle à la fin de la courbe. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> Courbe vers relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> Chemin d’accès fermé </p> </td> 
   <td> <p> Fermez le sous-chemin actuel par une ligne droite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les commandes en majuscules indiquent que les valeurs de coordonnées sont en pixels absolus (par rapport au coin supérieur gauche du rectangle du calque). Les décalages de pixels suivent les commandes en minuscules par rapport à la position actuelle.

« M » ou « M » commence toujours un nouveau sous-chemin. Les sous-chemins sont fermés automatiquement (avec une ligne droite) si &#39;Z&#39; ou &#39;z&#39; n’est pas spécifié à la fin.

Si un sous-chemin commence par un déplacement relatif vers (&#39;m&#39;), il est relatif à l’un des éléments suivants :

* Point de départ du sous-chemin précédent, s’il était fermé par « z » ou « Z ».
* Point d’arrivée du sous-chemin précédent, s’il n’a pas été fermé explicitement.
* 0,0, s’il s’agit du premier sous-chemin.

## Propriétés {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attribut de calque. S’applique au calque actif ou à l’image composite si `layer=comp`. Les calques d’effet l’ignorent.

Le modificateur `clipPathE=` est ignoré si aucun chemin portant le nom spécifié n’est trouvé dans l’image source du calque ou si la source du calque n’est pas une image.

## Par défaut {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Aucun, pour aucun écrêtage supplémentaire du calque.

## Voir aussi {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
