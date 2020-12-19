---
description: Profil de couleur de sortie par défaut en niveaux de gris. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleur en niveaux de gris spécifiées avec diverses commandes de traitement d’images, telles que color=.
seo-description: Profil de couleur de sortie par défaut en niveaux de gris. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleur en niveaux de gris spécifiées avec diverses commandes de traitement d’images, telles que color=.
seo-title: IccProfileGray
solution: Experience Manager
title: IccProfileGray
topic: Scene7 Image Serving - Image Rendering API
uuid: a7d40114-f91f-4637-bb49-5b06b9ce846d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---


# IccProfileGray{#iccprofilegray}

Profil de couleur de sortie par défaut en niveaux de gris. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleur en niveaux de gris spécifiées avec diverses commandes de traitement d’images, telles que color=.

## Propriétés {#section-03f090ee2acf4537b83f78840d23ecab}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès de fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil en niveaux de gris.

## Par défaut {#section-95ba3ab15edc4259b657c6ebf8783d61}

Hérité de `default::IccProfileGray` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
