---
title: IccProfileRgb
description: Profil de couleurs de sortie par défaut de RGB. Indique le nom du profil colorimétrique ICC à utiliser pour les images de réponse RGB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc=. Également pour certaines valeurs de couleur RGB spécifiées avec différentes commandes de rendu d’image, telles que bgc= et color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# IccProfileRgb{#iccprofilergb}

Profil de couleurs de sortie par défaut de RGB. Indique le nom du profil colorimétrique ICC à utiliser pour les images de réponse RGB lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec `icc=`. Également pour certaines valeurs de couleur RGB spécifiées avec différentes commandes de rendu d’image, telles que `bgc=` et `color=`.

## Propriétés {#section-b4a1bd92e99047479a5036413525a6d9}

Chaîne de texte. Si spécifié, doit être une valeur de `icc::Name` valide de la carte de profil ICC de ce catalogue de matières ou du catalogue par défaut, ou un chemin d&#39;accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil RGB.

## Par défaut {#section-5809772f8e96438ab7626d323c66a4ba}

Hérité de `default::IccProfileRgb` si non défini ou si vide.

## Voir aussi {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
