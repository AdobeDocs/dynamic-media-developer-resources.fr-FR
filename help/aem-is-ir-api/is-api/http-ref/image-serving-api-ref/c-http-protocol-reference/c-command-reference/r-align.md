---
title: aligner
description: Aligner l’image sur la vue. Aligne l’image composite (éventuellement après mise à l’échelle, si scl= est également spécifié) dans le rectangle d’affichage défini par les commandes wid= et hei=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
TQID: 'https://experienceleague.adobe.com/ZIogqM83I6NCYf8tQkCPuGDfhxZPq9aQXcgW4xR2lJE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 1%

---

# aligner{#align}

Aligner l’image sur la vue. Aligne l’image composite (éventuellement après mise à l’échelle, si scl= est également spécifié) dans le rectangle d’affichage défini par les commandes wid= et hei=.

` align= *`horiz`*, *`vert`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> horiz </span> </span> </p> </td> 
  <td class="stentry"> <p>alignement horizontal (réel, -1,0...1,0) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> vert </span> </span> </p> </td> 
  <td class="stentry"> <p>alignement vertical (réel, -1,0...1,0) </p> </td> 
 </tr> 
</table>

Indiquez `align=-1,-1` aligner le coin supérieur gauche de l’image composite avec le coin supérieur gauche de la vue, spécifiez `align=1,1` aligner le coin inférieur droit de l’image avec le coin inférieur droit de la vue. Pour les demandes d’image et de miniature standard, toute zone de la vue qui n’est pas couverte par des données d’image composites est remplie avec des `bgc=`.

## Propriétés {#section-3fbec8206fc944eda4746d8be84f3b41}

Attribut d’affichage. (`align=` est également utilisé pour définir l’alignement entre une image de filigrane et l’image composite à laquelle le filigrane est appliqué.) S’applique quel que soit le paramètre de calque actuel. Ignoré si un seul des `wid=` et `hei=` est spécifié et lorsqu’il est `fit=constrain` ou `fit=stretch`.

## Par défaut {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`, qui centre l’image dans le rectangle de vue.

## Exemple {#section-2c9447aa2e184fb8ab1a4370dc61d554}

La requête suivante s’adapte `myImage` dans un rectangle de vue de 200 x 200 pixels.

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

Si `myImage` est exactement carré, il remplit tout le rectangle de vue. Si `myImage` a un format portrait, il est mis à l’échelle pour faire 200 pixels de haut et est centré horizontalement dans la vue. Si `myImage` a un format de paysage, il est mis à l’échelle sur une largeur de 200 pixels et est aligné sur le bord supérieur de la vue. Dans tous les cas, l’image renvoyée fait exactement 200 x 200 pixels ; tout espace non couvert par le `myImage` mis à l’échelle est rempli de `attribute::BkgColor` (spécifiez bgc= pour contrôler dynamiquement la couleur d’arrière-plan).

## Voir aussi {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Watermarks](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
