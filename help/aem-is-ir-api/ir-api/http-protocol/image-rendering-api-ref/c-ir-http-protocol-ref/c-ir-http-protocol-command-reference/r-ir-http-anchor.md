---
title: ancrage
description: Ancre d’image (zone réactive). Indique le point d’ancrage de texture (zone réactive) de la texture répétable ou de la matière de vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---

# ancrage{#anchor}

Ancre d’image (zone réactive). Indique le point d’ancrage de texture (zone réactive) de la texture répétable ou de la matière de vignette.

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`yn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>Décalage en pixels à partir du coin supérieur gauche de l’image source (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>Décalage normalisé par rapport au centre de l’image source (réel, réel). </p></td> 
 </tr> 
</table>

Une texture répétable est appliquée à un objet vignette, de sorte que le point d&#39;ancrage de texture ( `anchor=`) se trouve au point d&#39;origine de texture de l&#39;objet.

Une image de vignette est appliquée à un objet vignette, de sorte que le point d&#39;ancrage de la vignette se trouve au point d&#39;origine de la vignette de l&#39;objet. La position de la vignette peut être ajustée à l&#39;aide de la commande `pos=`.

`anchorN=0,0` Place l’ancre d’image au centre de l’image source. `anchorN=-0.5,-0.5` ou `anchor=0,0` se trouve dans le coin supérieur gauche et `anchorN=0.5,0.5` dans le coin inférieur droit de l’image source.

## Propriétés {#section-91f929d35cd745ab9e1eeecf45fcedae}

**Attribut Material**. Ignoré si `align=2` ou si le matériau n&#39;est pas une texture répétable, un papier peint ou une vignette.

## Par défaut {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, si le matériau est basé sur une entrée de catalogue. Sinon, `anchor=0,0` (le coin supérieur gauche de l’image) pour les textures et les papiers peints répétables, et `anchorN=0,0` (le centre de l’image) pour les autocollants.

## Voir aussi {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
