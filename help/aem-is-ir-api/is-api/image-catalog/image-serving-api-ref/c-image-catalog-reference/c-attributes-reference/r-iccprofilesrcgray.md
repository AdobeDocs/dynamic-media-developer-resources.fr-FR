---
description: Profil de couleur d’entrée par défaut en niveaux de gris. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source en niveaux de gris qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs en niveaux de gris spécifiées avec diverses commandes de traitement d’images, telles que color=.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Profil de couleur d’entrée par défaut en niveaux de gris. Spécifie le nom du profil de couleurs ICC à utiliser pour les images source en niveaux de gris qui n’incorporent pas de profil de couleurs et pour certaines valeurs de couleurs en niveaux de gris spécifiées avec diverses commandes de traitement d’images, telles que color=.

## Propriétés {#section-8cbb316df6eb463aaca7b308d3568086}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès de fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil en niveaux de gris.

## Par défaut {#section-bcc7250715884412bd0780f60d1cce7b}

Hérité de `default::IccProfileSrcGray` si elle n&#39;est pas définie ou si elle est vide. Si `attribute::IccProfileSrcGray` ne correspond pas à un profil valide, `attribute::IccProfileGray` est utilisé à la place.

## Voir aussi {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
