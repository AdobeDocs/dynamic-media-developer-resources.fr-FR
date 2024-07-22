---
title: IccProfileSrcCmyk
description: Profil colorimétrique d’entrée par défaut CMJN. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source CMJN qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Profil colorimétrique d’entrée par défaut CMJN. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source CMJN qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.

## Propriétés {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant de la carte de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Hérité de `default::IccProfileSrcCmyk` si elle n’est pas définie ou si elle est vide. Si `attribute::IccProfileSrcCmyk` ne se résout pas en un profil valide, `attribute::IccProfileCmyk` est utilisé à la place.

## Voir aussi {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
