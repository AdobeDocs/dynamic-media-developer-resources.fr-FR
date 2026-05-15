---
title: src
description: Image du calque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
TQID: 'https://experienceleague.adobe.com/4BChH5cLIy-7A3mnQqqo0S7Z4XfoC4T-34gI-YM-tGY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 2%

---

# src{#src}

Image du calque.

` src= *`object`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de l’objet <span class="varname"> </p> </td> 
  <td class="stentry"> <p>Objet image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </span> de <span class="varname"> nestedRequest </p> </td> 
  <td class="stentry"> <p>Diffusion d’images imbriquées, rendu d’images ou requête externe. </p> </td> 
 </tr> 
</table>

## Description {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Indique l’image source d’un calque d’image.

*`object`* peut s’agir d’une entrée de catalogue ou d’un fichier image/SVG.

Voir [objet](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Les requêtes imbriquées ou incorporées sont entourées d’accolades. Préfixez une requête de diffusion d’images incorporée avec `is`, une requête de rendu d’images incorporée avec `ir` et une requête de rendu de graphiques FXG avec `fxg`. Une requête vers un serveur étranger est supposée si aucun préfixe n’est spécifié.

Voir [Demande d’imbrication et d’incorporation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Propriétés {#section-2c22bb89a35d470f833df8ba898efd93}

Attribut de calque. S’applique aux `layer=0` si `layer=comp`. Mutuellement exclusif avec `text=` et `textPs=` dans le même calque ; la dernière occurrence de `text=`, `textPs=` ou `src=` prévaut et détermine s’il s’agit d’un calque d’image ou de texte. Ignoré par les calques d’effet.

*`object`* ne peut pas être résolu sur un autre enregistrement de catalogue qui inclut une commande `src=` ou `mask=` dans son `catalog::Modifier`. (Utilisez l’imbrication de requêtes pour obtenir un effet similaire.)

Les préfixes `is`, `ir` et `fxg` respectent la casse.

## Par défaut {#section-a92f3882041b4d43ae2caf014647165f}

Pour le calque 0, l’objet du composant de chemin de l’URL est utilisé si `src=` n’est pas spécifié. Aucune valeur par défaut pour les autres calques.

## Voir aussi {#section-e467e03330564796932ac081f1c9c1d0}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [object](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Request Nested et Embedding](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
