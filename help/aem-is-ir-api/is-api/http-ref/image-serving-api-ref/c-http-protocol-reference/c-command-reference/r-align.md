---
description: Aligner l’image avec les . Aligne l’image composite (éventuellement après la mise à l’échelle, si scl= est également spécifié) dans le rectangle  défini par wid= et hei=.
seo-description: Aligner l’image avec les . Aligne l’image composite (éventuellement après la mise à l’échelle, si scl= est également spécifié) dans le rectangle  défini par wid= et hei=.
seo-title: aligner
solution: Experience Manager
title: aligner
topic: Scene7 Image Serving - Image Rendering API
uuid: 91940bd4-8e2b-4949-a76d-31cd238783bc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# align{#align}

Aligner l’image avec les . Aligne l’image composite (éventuellement après la mise à l’échelle, si scl= est également spécifié) dans le rectangle  défini par wid= et hei=.

` align= *``*, *`horizontal`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span></span> </p> </td> 
  <td class="stentry"> <p>alignement horizontal (réel, -1.0...1.0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span></span> </p> </td> 
  <td class="stentry"> <p>alignement vertical (réel, -1.0...1.0) </p> </td> 
 </tr> 
</table>

Spécifiez `align=-1,-1` pour aligner l’image composite en haut à gauche de l’, `align=1,1` pour aligner l’image en bas à droite de l’image avec l’en bas à droite de l’. Pour les demandes d’image et de miniature standard, toute zone du qui n’est pas couverte par les données d’image composite est remplie `bgc=`.

## Propriétés {#section-3fbec8206fc944eda4746d8be84f3b41}

attribut . ( `align=` sert également à définir l’alignement entre une image de filigrane et l’image composite à laquelle le filigrane est appliqué.) S’applique indépendamment du paramètre de calque actif. Ignoré si seul l’un des `wid=` et `hei=` est spécifié et quand `fit=constrain` ou `fit=stretch`.

## Par défaut {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, qui centre l’image dans le rectangle  du.

## Exemple {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La requête suivante s’adapte `myImage` à un rectangle de 200 x 200 pixels de.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Si `myImage` elle est exactement carrée, elle remplit tout le rectangle  du. Si `myImage` le rapport L/H en mode portrait est défini sur 200 pixels, il est centré horizontalement dans le . Si `myImage` le rapport L/H en mode paysage est défini sur 200 pixels de largeur, il est aligné sur le bord supérieur du . Dans tous les cas, la taille de l’image renvoyée est exactement de 200 x 200 pixels ; tout espace non couvert par la mise à l’échelle `myImage` est rempli avec `attribute::BkgColor` (spécifiez bgc= pour contrôler dynamiquement la couleur d’arrière-plan).

## Voir aussi {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), Filigranes[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
