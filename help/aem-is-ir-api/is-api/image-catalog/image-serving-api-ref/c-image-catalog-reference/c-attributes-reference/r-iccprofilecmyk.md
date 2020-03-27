---
description: de couleurs de sortie par défaut CMJN. Indique le nom du de couleurs ICC à utiliser pour les images de réponse CMJN lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.
seo-description: de couleurs de sortie par défaut CMJN. Indique le nom du de couleurs ICC à utiliser pour les images de réponse CMJN lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileCmyk{#iccprofilecmyk}

de couleurs de sortie par défaut CMJN. Indique le nom du de couleurs ICC à utiliser pour les images de réponse CMJN lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de diffusion d’images, telles que color=.

## Propriétés {#section-d8b6102cc1c744d482f99808ccfcaa24}

Chaîne de texte. Le cas échéant, doit correspondre à une `icc::Name` valeur valide de la carte de  ICC de ce catalogue d’images ou du catalogue par défaut, ou à un chemin d’accès de fichier relatif à `attribute::RootPath`. Le ICC référencé doit être un CMJN .

## Par défaut {#section-62442df09a724950bfbdd0640b3e6678}

Héritée de `default::IccProfileCmyk` si non définie ou si vide.

## Voir aussi {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribut::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribut::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [attribut::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
