---
description: Aligner l’image avec la Vue. Aligne l’image composite (éventuellement après la mise à l’échelle, si scl= est également spécifié) dans le rectangle de la vue défini par wid= et hei=.
solution: Experience Manager
title: aligner
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 1%

---


# align{#align}

Aligner l’image avec la Vue. Aligne l’image composite (éventuellement après la mise à l’échelle, si scl= est également spécifié) dans le rectangle de la vue défini par wid= et hei=.

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

Spécifiez `align=-1,-1` pour aligner l’image composite en haut à gauche de la vue, `align=1,1` pour aligner l’image en bas à droite de l’image avec l’en bas à droite de la vue. Pour les demandes d’image et de miniature standard, toute zone de la vue qui n’est pas couverte par les données d’image composite est remplie avec `bgc=`.

## Propriétés {#section-3fbec8206fc944eda4746d8be84f3b41}

Attribut de vue. ( `align=` est également utilisé pour définir l’alignement entre une image de filigrane et l’image composite à laquelle le filigrane est appliqué.) S’applique quel que soit le paramètre de calque actif. Ignoré si un seul des `wid=` et `hei=` est spécifié et quand `fit=constrain` ou `fit=stretch`.

## Par défaut {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, qui centre l’image dans le rectangle de la vue.

## Exemple {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La requête suivante tient `myImage` dans un rectangle de vue de 200 x 200 pixels.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Si `myImage` est exactement carré, il remplit tout le rectangle de la vue. Si `myImage` présente un rapport L/H en mode portrait, il est mis à l’échelle avec une hauteur de 200 pixels et est centré horizontalement dans la vue. Si `myImage` présente un format paysage, il est mis à l’échelle avec une largeur de 200 pixels et est aligné sur le bord supérieur de la vue. Dans tous les cas, la taille de l’image renvoyée est exactement de 200 x 200 pixels ; tout espace non couvert par l&#39;échelle `myImage` est rempli de `attribute::BkgColor` (indiquez bgc= pour contrôler dynamiquement la couleur d&#39;arrière-plan).

## Voir aussi {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), Filigranes](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)[
