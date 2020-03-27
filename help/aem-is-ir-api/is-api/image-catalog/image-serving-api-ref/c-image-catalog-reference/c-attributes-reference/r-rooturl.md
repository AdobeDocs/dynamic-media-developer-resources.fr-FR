---
description: URL racine pour les URL d’image relatives. Indique l’URL racine des URL d’image relatives.
seo-description: URL racine pour les URL d’image relatives. Indique l’URL racine des URL d’image relatives.
seo-title: RootUrl
solution: Experience Manager
title: RootUrl
topic: Scene7 Image Serving - Image Rendering API
uuid: 173ce99a-f87e-4700-a28a-1a87b8c55b85
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# RootUrl{#rooturl}

URL racine pour les URL d’image relatives. Indique l’URL racine des URL d’image relatives.

`attribute::RootUrl` est utilisée à la place de `attribute::RootPath` lorsqu’une `src=` ou `mask=` valeur est entourée de {accolades} ou (parenthèses).

## Propriétés {#section-fe02269b4b724319a5d1f2cfcae31cba}

Valeur de chaîne de texte. Chemin d’accès racine de l’URL absolue, y compris l’identifiant de protocole de début. Les protocoles suivants sont pris en charge : HTTP, HTTPS et FTP.

## Par défaut {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Hérité de `default::RootUrl` si non définie. S’ils sont définis mais vides, les URL relatives ne sont pas prises en charge par ce catalogue d’images.

## Voir aussi {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)[, jeu de règles::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
