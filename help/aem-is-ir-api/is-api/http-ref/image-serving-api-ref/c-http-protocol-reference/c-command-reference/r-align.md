---
description: Aligner l’image avec la vue. Aligne l’image composite (éventuellement après la mise à l’échelle, si scl= est également spécifié) dans le rectangle de l’affichage défini par wid= et hei=.
solution: Experience Manager
title: align
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 1%

---

# align{#align}

Aligner l’image avec la vue. Aligne l’image composite (éventuellement après la mise à l’échelle, si scl= est également spécifié) dans le rectangle de l’affichage défini par wid= et hei=.

` align= *``*, *`horizontal`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz  </span> </span> </p> </td> 
  <td class="stentry"> <p>alignement horizontal (réel, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert  </span> </span> </p> </td> 
  <td class="stentry"> <p>alignement vertical (réel, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Spécifiez `align=-1,-1` pour aligner le coin supérieur gauche de l’image composite avec le coin supérieur gauche de l’affichage, spécifiez `align=1,1` pour aligner le coin inférieur droit de l’image avec le coin inférieur droit de l’affichage. Pour les demandes d’image standard et de miniature, toute zone de la vue qui n’est pas couverte par les données d’image composite est remplie avec `bgc=`.

## Propriétés {#section-3fbec8206fc944eda4746d8be84f3b41}

Attribut d’affichage. ( `align=` est également utilisé pour définir l’alignement entre une image de filigrane et l’image composite à laquelle le filigrane est appliqué.) S’applique quel que soit le paramètre de calque actif. Ignoré si un seul des `wid=` et `hei=` est spécifié et quand `fit=constrain` ou `fit=stretch`.

## Par défaut {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, qui centre l’image dans le rectangle de l’affichage.

## Exemple {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La requête suivante correspond à `myImage` dans un rectangle d’affichage de 200 x 200 pixels.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Si `myImage` est exactement carré, il remplit tout le rectangle de la vue. Si `myImage` présente un rapport L/H portrait, il est mis à l’échelle pour une hauteur de 200 pixels et est centré horizontalement dans la vue. Si `myImage` présente un rapport d’aspect paysage, il est dimensionné pour une largeur de 200 pixels et est aligné sur le bord supérieur de la vue. Dans tous les cas, la taille de l’image renvoyée est exactement de 200 x 200 pixels ; tout espace non couvert par la balise `myImage` mise à l’échelle est rempli de `attribute::BkgColor` (spécifiez bgc= pour contrôler dynamiquement la couleur d’arrière-plan).

## Voir aussi {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Filigranes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
