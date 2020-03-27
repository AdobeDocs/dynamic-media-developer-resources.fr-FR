---
description: de couleur d’entrée par défaut en niveaux de gris. Indique le nom du de couleurs ICC à utiliser pour les images source en niveaux de gris qui n’incorporent pas de de couleurs et pour certaines valeurs de couleurs en niveaux de gris spécifiées avec diverses commandes de diffusion d’images, telles que color=.
seo-description: de couleur d’entrée par défaut en niveaux de gris. Indique le nom du de couleurs ICC à utiliser pour les images source en niveaux de gris qui n’incorporent pas de de couleurs et pour certaines valeurs de couleurs en niveaux de gris spécifiées avec diverses commandes de diffusion d’images, telles que color=.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

de couleur d’entrée par défaut en niveaux de gris. Indique le nom du de couleurs ICC à utiliser pour les images source en niveaux de gris qui n’incorporent pas de de couleurs et pour certaines valeurs de couleurs en niveaux de gris spécifiées avec diverses commandes de diffusion d’images, telles que color=.

## Propriétés {#section-8cbb316df6eb463aaca7b308d3568086}

Chaîne de texte. Le cas échéant, doit correspondre à une `icc::Name` valeur valide de la carte de  ICC de ce catalogue d’images ou du catalogue par défaut, ou à un chemin d’accès de fichier relatif à `attribute::RootPath`. Le  ICC référencé doit être un en niveaux de gris.

## Par défaut {#section-bcc7250715884412bd0780f60d1cce7b}

Héritée de `default::IccProfileSrcGray` si non définie ou si vide. Si `attribute::IccProfileSrcGray` la résolution ne correspond pas à un  valide, `attribute::IccProfileGray` est utilisé à la place.

## Voir aussi {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribut::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribut::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35), [attribut::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
