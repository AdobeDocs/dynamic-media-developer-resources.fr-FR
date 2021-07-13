---
description: Profil colorimétrique de sortie RVB par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse RVB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de diffusion d’images, telles que color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

Profil colorimétrique de sortie RVB par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse RVB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de diffusion d’images, telles que color=.

## Propriétés {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil RVB.

## Par défaut {#section-dfe08dd7b851453ca816623a4179955b}

Hérité de `default::IccProfileRgb` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
