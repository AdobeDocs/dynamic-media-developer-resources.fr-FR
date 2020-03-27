---
description: ' de couleurs de sortie RVB par défaut. Indique le nom du de couleurs ICC à utiliser pour les images de réponse RVB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de rendu d’image, telles que bgc= et color=.'
seo-description: ' de couleurs de sortie RVB par défaut. Indique le nom du de couleurs ICC à utiliser pour les images de réponse RVB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de rendu d’image, telles que bgc= et color=.'
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fe63607-c328-468a-aa55-0c4d16cf9f0f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileRgb{#iccprofilergb}

 de couleurs de sortie RVB par défaut. Indique le nom du de couleurs ICC à utiliser pour les images de réponse RVB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de rendu d’image, telles que bgc= et color=.

## Propriétés {#section-b4a1bd92e99047479a5036413525a6d9}

Chaîne de texte. Si spécifié, doit être une `icc::Name` valeur valide du mappage de  ICC de ce catalogue de matériaux ou du catalogue par défaut, ou un chemin d’accès de fichier relatif à `attribute::RootPath`. Le ICC référencé doit être un RVB .

## Par défaut {#section-5809772f8e96438ab7626d323c66a4ba}

Héritée de `default::IccProfileRgb` si non définie ou si vide.

## Voir aussi {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribut::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribut::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribut::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
