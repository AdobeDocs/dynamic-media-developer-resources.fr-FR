---
description: Texte du calque (compatible avec Adobe Photoshop). Indique le corps de texte d’un calque de texte.
solution: Experience Manager
title: textPs
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 4%

---

# textPs{#textps}

Texte du calque (compatible avec Adobe Photoshop). Indique le corps de texte d’un calque de texte.

`textPs= *`chaîne`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> string</span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne au format texte enrichi (RTF). </p></td> 
 </tr> 
</table>

Toutes les commandes de police, de couleur de police et de mise en forme de paragraphe sont effectuées à l’aide des commandes RTF.

Voir [Formatage du texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` prend en charge des fonctionnalités étendues, telles que la justification, le flux de texte dans des régions non rectangulaires définies avec  `textFlowPath=` et/ou  `textFlowXPath=`, et le rendu de texte le long de chemins arbitraires définis avec  `textPath=`.

## Propriétés {#section-a289dc26b6534b41998b1e241d5f2f92}

Attribut de calque. S’applique à `layer=0` si `layer=comp`. Mutuellement exclusive avec `src=` et `text=` dans le même calque. La dernière occurrence de `text=`, `textPs=` et `src=` prévaut et détermine s’il s’agit d’une image ou d’un calque de texte. Ignoré par les calques d’effet.

## Par défaut {#section-11c2ae2c96d64a0a9c207252df663e4d}

Aucune

## Voir aussi {#section-5c2b25767d2b47b5be817271ab12e13c}

[Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542),  [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
