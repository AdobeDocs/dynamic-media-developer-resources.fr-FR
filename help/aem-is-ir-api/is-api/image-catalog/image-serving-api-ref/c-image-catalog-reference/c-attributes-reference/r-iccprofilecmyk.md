---
description: PROFIL de couleur de sortie par défaut CMJN. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse CMJN lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de traitement d’images, telles que color=.
seo-description: PROFIL de couleur de sortie par défaut CMJN. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse CMJN lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de traitement d’images, telles que color=.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---


# IccProfileCmyk{#iccprofilecmyk}

PROFIL de couleur de sortie par défaut CMJN. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse CMJN lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs CMJN spécifiées avec diverses commandes de traitement d’images, telles que color=.

## Propriétés {#section-d8b6102cc1c744d482f99808ccfcaa24}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès de fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-62442df09a724950bfbdd0640b3e6678}

Hérité de `default::IccProfileCmyk` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
