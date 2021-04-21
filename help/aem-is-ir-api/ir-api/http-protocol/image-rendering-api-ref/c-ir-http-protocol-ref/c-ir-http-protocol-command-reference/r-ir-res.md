---
description: Résolution de matériau. Indique la résolution de la texture ou de l’image de décale répétable.
solution: Experience Manager
title: res
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# res{#res}

Résolution de matériau. Indique la résolution de la texture ou de l’image de décale répétable.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Résolution ; unités de résolution de matériau (généralement pixels par pouce) (réel). </p> </td> 
 </tr> 
</table>

Dans le cas d&#39;un matériau de décomposition, `size=` l&#39;emporte si `size=` et `res=` sont spécifiés.

## Propriétés {#section-6a458ddc202f46e0b668c9f040a65cef}

Attribut de matériau. Ignoré par les matériaux de couleur unie. Uniquement par armoire et garnitures de fenêtre uniquement si une texture est également utilisée.

## Par défaut {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, si le matériau est basé sur une entrée de catalogue, sinon  `attribute::Resolution`, si  `res= is` non spécifié ou défini sur une valeur inférieure ou égale à 0.

## Voir aussi {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Résolution](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b) du matériau,  [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988),  [catalog::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7),  [attribut::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
