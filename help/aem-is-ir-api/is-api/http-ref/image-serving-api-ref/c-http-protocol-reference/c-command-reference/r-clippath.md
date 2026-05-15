---
title: clipPath
description: Chemin d’accès du clip de calque. Spécifie une trajectoire d’élément pour le calque actif.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
TQID: 'https://experienceleague.adobe.com/K4w8R8Ke-0GXFdhfpxgAcltyN3icVsJJdRGfx1OiSjg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 556
ht-degree: 0%

---

# clipPath{#clippath}

Chemin d’accès du clip de calque. Spécifie une trajectoire d’élément pour le calque actif.

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition </span> </span> </p> </td> 
  <td class="stentry"> <p>Données de chemin. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>Nom du chemin incorporé dans l’image source du calque (ASCII uniquement). </p></td> 
 </tr> 
</table>

Toute partie du calque située en dehors de la zone définie par `clipPath=` est rendue transparente.

`*`pathName`*` est le nom d’un chemin d’accès incorporé dans l’image source du calque. Le chemin est automatiquement transformé pour conserver un alignement relatif avec le contenu de l’image. Si plusieurs `*`pathName`*` sont spécifiés, le serveur tronque l’image à l’intersection de ces chemins. Tout `*`pathName`*` introuvable dans l’image source est ignoré.

>[!NOTE]
>
>Seules les chaînes ASCII sont prises en charge pour `*`pathName`*`.

`*`pathDefinition`*` permet de spécifier des données de chemin explicites dans les coordonnées des pixels du calque.

Si `size=` est spécifié et non 0,0, le calque est prédimensionné. Dans ce cas, les coordonnées de tracé sont relatives au coin supérieur gauche du rectangle du calque et le calque est positionné en fonction de `origin=` ou de sa valeur par défaut. Toutes les zones du tracé situées en dehors du rectangle du calque restent transparentes.

Si `size=` n’est pas spécifié pour un calque de texte ou de couleur unie, le calque est considéré comme auto-dimensionné, l’étendue du chemin déterminant sa taille. Si `origin=` n’est pas spécifié, la valeur par défaut est (0,0) de l’espace des coordonnées du chemin. Ce processus de workflow permet de spécifier les coordonnées du chemin par rapport à l’origine du calque 0.

>[!NOTE]
>
>Les commandes `scale=`, `rotate=` et `anchor=` ne sont pas autorisées pour le redimensionnement automatique des calques de couleur unie.

`*`pathDefinition`*` accepte une chaîne similaire à la valeur de l’attribut `d=` de l’élément de `<path>` SVG, sauf que des virgules sont utilisées à la place des espaces pour séparer les valeurs. `*`pathDefinition`*` peut inclure un ou plusieurs sous-chemins en boucle fermée.

Les commandes de chemin suivantes sont prises en charge dans `*`pathDefinition`*` :

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> Commande </b> <b></th> 
   <th class="entry"> <b> Name </b> </th> 
   <th class="entry"> <b> Description </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> M</b> <span class="varname"> x,y</span> </td> 
   <td> <p> passer à l’absolu </p> </td> 
   <td> <p> Démarrer un nouveau sous-chemin à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> déplacer vers un relatif </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto absolu </p> </td> 
   <td> <p> Trace une ligne de la position actuelle à x,y. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> linéaire par rapport </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> curveto absolu </p> </td> 
   <td> <p> Tracez une courbe de Bézier de la position actuelle à x,y. x1,y1 est le point de contrôle au début de la courbe et x2,y2 est le point de contrôle à la fin de la courbe. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> courbure relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> cheminement étroit </p> </td> 
   <td> <p> Ferme le sous-tracé actif avec une ligne droite. </p> </td> 
  </tr> 
 </tbody> 
</table>

Les commandes en majuscules indiquent que les valeurs des coordonnées sont dans des positions absolues en pixels (par rapport au coin supérieur gauche du rectangle du calque). Les décalages en pixels suivent des commandes en minuscules par rapport à la position actuelle.

&#39;m&#39; ou &#39;M&#39; lance toujours un nouveau sous-chemin. Les sous-chemins sont fermés automatiquement (avec une ligne droite) si &#39;Z&#39; ou &#39;z&#39; n&#39;est pas spécifié à la fin.

Si un sous-chemin commence par un déplacement relatif vers (’m’), il est relatif à l’un des éléments suivants :

* Point de départ du sous-chemin précédent, s’il était fermé par « z » ou « Z ».
* Point de fin du sous-chemin précédent, s’il n’a pas été fermé explicitement.
* 0,0, s’il s’agit du premier sous-chemin.

## Propriétés {#section-d4127db0dac54e3cbd44f7ea1e001960}

Attribut de calque. S’applique au calque actif ou à l’image composite, le cas `layer=comp`. Les calques d’effet l’ignorent.

Le `clipPathE=` de modificateur est ignoré si aucun chemin portant le nom spécifié n&#39;est trouvé dans l&#39;image source du calque ou si la source du calque n&#39;est pas une image.

## Par défaut {#section-076c35ea37fa4a44ada253b4c2dec1dd}

Aucun, pour aucun écrêtage supplémentaire du calque.

## Voir aussi {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
