---
description: Image de calque.
solution: Experience Manager
title: src
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 3%

---

# src{#src}

Image de calque.

` src= *``*|{[is|ir|fxg]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> objet </span> </p> </td> 
  <td class="stentry"> <p>Objet image. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest  </span> </p> </td> 
  <td class="stentry"> <p>Serveur d’images imbriqué, rendu d’images ou requête externe. </p> </td> 
 </tr> 
</table>

## Description {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Indique l’image source d’un calque d’image.

*`object`* Il peut s’agir d’une entrée de catalogue ou d’un fichier image/SVG.

Voir [objet](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

Les requêtes imbriquées ou incorporées sont entourées d’accolades. Préfixez une requête de diffusion d’images incorporée avec `is`, une requête de rendu d’images incorporée avec `ir` et une requête de rendu d’images FXG avec `fxg`. Une requête à un serveur étranger est supposée si aucun préfixe n’est spécifié.

Voir [Imbrication de requêtes et incorporation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Propriétés {#section-2c22bb89a35d470f833df8ba898efd93}

Attribut de calque. S’applique à `layer=0` si `layer=comp`. Mutuellement exclusif avec `text=` et `textPs=` dans le même calque ; la dernière occurrence de `text=`, `textPs=` ou `src=` prévaut et détermine s’il s’agit d’une image ou d’un calque de texte. Ignoré par les calques d’effet.

*`object`*ne peut pas se résoudre par un autre enregistrement de catalogue qui inclut une commande `src=` ou `mask=` dans son `catalog::Modifier`. (Utilisez l’imbrication de requêtes pour obtenir un effet similaire.)

Les préfixes `is`, `ir` et `fxg` sont sensibles à la casse.

## Par défaut {#section-a92f3882041b4d43ae2caf014647165f}

Pour la couche 0, l’objet du composant de chemin de l’URL est utilisé si `src=` n’est pas spécifié. Aucune valeur par défaut pour les autres calques.

## Voir aussi {#section-e467e03330564796932ac081f1c9c1d0}

[catalogue ::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [attribut::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [objet](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [Modèles](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [Imbrication de requête et Incorporation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
