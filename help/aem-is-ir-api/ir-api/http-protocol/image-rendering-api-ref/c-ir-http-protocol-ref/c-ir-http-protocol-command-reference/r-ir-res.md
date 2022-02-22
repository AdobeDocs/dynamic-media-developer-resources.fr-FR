---
title: res
description: Résolution des matériaux. Indique la résolution de la texture ou de l’image décale répétable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# res{#res}

Résolution des matériaux. Indique la résolution de la texture ou de l’image décale répétable.

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Résolution; unités de résolution du matériau (généralement pixels par pouce) (réel). </p> </td> 
 </tr> 
</table>

S&#39;il y a un matériau décal, `size=` prévaut si les deux `size=` et `res=` sont spécifiées.

## Propriétés {#section-6a458ddc202f46e0b668c9f040a65cef}

Attribut de matière. Ignoré par les matériaux couleur solides. Uniquement par des armoires et des revêtements de fenêtre que si une texture est également utilisée.

## Par défaut {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`, si le matériau est basé sur une entrée de catalogue, sinon `attribute::Resolution`, si `res= is` non spécifié ou défini sur une valeur inférieure ou égale à 0.

## Voir aussi {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[Résolution des matériaux](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b), [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988), [catalogue : résolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
