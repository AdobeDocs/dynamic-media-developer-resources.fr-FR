---
description: Profil de couleur d’entrée RVB par défaut. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source RVB qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de traitement d’images, telles que color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

Profil de couleur d’entrée RVB par défaut. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source RVB qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de traitement d’images, telles que color=.

## Propriétés {#section-3cd753196959462e9e674dab0b033d08}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès de fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil RVB.

## Par défaut {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Hérité de `default::IccProfileSrcRgb` si elle n&#39;est pas définie ou si elle est vide. Si `attribute::IccProfileSrcRgb` ne correspond pas à un profil valide, `attribute::IccProfileRgb` est utilisé à la place.

## Voir aussi {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
