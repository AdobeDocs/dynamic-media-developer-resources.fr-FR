---
title: textPs
description: Texte du calque (compatible avec Adobe Photoshop). Indique le corps de texte d’un calque de texte.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
TQID: 'https://experienceleague.adobe.com/z5z7-6Pe4B-DUsxcspNcMxS-gXXo8Cv7stwBEMpxnNo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 3%

---

# textPs{#textps}

Texte du calque (compatible avec Adobe Photoshop). Indique le corps de texte d’un calque de texte.

`textPs= *`chaîne`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> string </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne RTF (Rich-text-formatted). </p></td> 
 </tr> 
</table>

Tous les contrôles de police, de couleur de police et de mise en forme de paragraphe sont réalisés à l’aide des commandes RTF.

Voir [Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` prend en charge des fonctions étendues, telles que la justification, le déplacement de texte dans des zones non rectangulaires définies avec des `textFlowPath=` et/ou des `textFlowXPath=`, et le rendu de texte le long de chemins arbitraires définis avec des `textPath=`.

## Propriétés {#section-a289dc26b6534b41998b1e241d5f2f92}

Attribut de calque. S’applique aux `layer=0` si `layer=comp`. Mutuellement exclusif avec `src=` et `text=` dans le même calque. La dernière occurrence de `text=`, `textPs=` et `src=` prévaut et détermine s’il s’agit d’un calque d’image ou de texte. Ignoré par les calques d’effet.

## Par défaut {#section-11c2ae2c96d64a0a9c207252df663e4d}

Aucune

## Voir aussi {#section-5c2b25767d2b47b5be817271ab12e13c}

[Formatage de texte](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
