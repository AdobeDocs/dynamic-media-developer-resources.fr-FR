---
description: PROFIL de couleur d’entrée CMJN par défaut. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source CMJN qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de traitement d’images, telles que color=.
solution: Experience Manager
title: IccProfileSrcCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

PROFIL de couleur d’entrée CMJN par défaut. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source CMJN qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de traitement d’images, telles que color=.

## Propriétés {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès de fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Hérité de `default::IccProfileSrcCmyk` si elle n&#39;est pas définie ou si elle est vide. Si `attribute::IccProfileSrcCmyk` ne correspond pas à un profil valide, `attribute::IccProfileCmyk` est utilisé à la place.

## Voir aussi {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
