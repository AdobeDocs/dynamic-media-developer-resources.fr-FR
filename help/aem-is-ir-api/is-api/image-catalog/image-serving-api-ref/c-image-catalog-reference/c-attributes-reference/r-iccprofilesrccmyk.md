---
description: de couleurs d’entrée CMJN par défaut. Indique le nom du de couleurs ICC à utiliser pour les images source CMJN qui n’incorporent pas de de couleurs et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.
seo-description: de couleurs d’entrée CMJN par défaut. Indique le nom du de couleurs ICC à utiliser pour les images source CMJN qui n’incorporent pas de de couleurs et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

de couleurs d’entrée CMJN par défaut. Indique le nom du de couleurs ICC à utiliser pour les images source CMJN qui n’incorporent pas de de couleurs et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.

## Propriétés {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Chaîne de texte. Le cas échéant, doit correspondre à une `icc::Name` valeur valide de la carte de  ICC de ce catalogue d’images ou du catalogue par défaut, ou à un chemin d’accès de fichier relatif à `attribute::RootPath`. Le ICC référencé doit être un CMJN .

## Par défaut {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Héritée de `default::IccProfileSrcCmyk` si non définie ou si vide. Si `attribute::IccProfileSrcCmyk` la résolution ne correspond pas à un  valide, `attribute::IccProfileCmyk` est utilisé à la place.

## Voir aussi {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribut::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribut::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribut::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
