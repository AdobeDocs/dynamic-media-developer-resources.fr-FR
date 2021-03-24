---
description: Profil de couleur de sortie RVB par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse RVB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de rendu d’image, telles que bgc= et color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# IccProfileRgb{#iccprofilergb}

Profil de couleur de sortie RVB par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse RVB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc= et pour certaines valeurs de couleurs RVB spécifiées avec diverses commandes de rendu d’image, telles que bgc= et color=.

## Propriétés {#section-b4a1bd92e99047479a5036413525a6d9}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue de matières ou du catalogue par défaut, ou un chemin d&#39;accès de fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil RVB.

## Par défaut {#section-5809772f8e96438ab7626d323c66a4ba}

Hérité de `default::IccProfileRgb` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
