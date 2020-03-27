---
description: Accentuer la texture. Indique l’accentuation à appliquer lors du rendu de ce matériau.
seo-description: Accentuer la texture. Indique l’accentuation à appliquer lors du rendu de ce matériau.
seo-title: aigu
solution: Experience Manager
title: aigu
topic: Scene7 Image Serving - Image Rendering API
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sharp{#sharp}

Accentuer la texture. Indique l’accentuation à appliquer lors du rendu de ce matériau.

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>01 </p> </td> 
  <td class="stentry"> <p>Pas d’accentuation. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Accentuation normale (tardive). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0 accentuation alternative (précoce). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Accentuation (précoce et tardive). </p> </td> 
 </tr> 
</table>

`sharp=1` applique l&#39;accentuation une fois le matériau rendu; applique l’accentuation après la mise à l’échelle initiale de la texture, mais avant qu’elle ne soit transformée en scène ; `sharp=2` `sharp=3` applique l’accentuation avant et après la transformation.

L’algorithme d’accentuation et la quantité d’accentuation et les autres paramètres USM (masquage flou) sont contrôlés par le modèle de matériau par défaut fourni par la vignette ou avec `rs=`.

## Propriétés {#section-498ec9fcb8eb415fb99532d36c11d4c7}

Attribut de matière. Ignoré par les matériaux de couleur unie.

## Par défaut {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, si le matériau est basé sur une entrée de catalogue, sinon `attribute::Sharp`.

## Voir aussi {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalogue ::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
