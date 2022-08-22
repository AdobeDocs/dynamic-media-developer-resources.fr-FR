---
title: IccProfileSrcRgb
description: Profil colorimétrique d’entrée par défaut du RGB. Indique le nom du profil de couleurs ICC à utiliser pour les images et les vignettes de matériaux RGB qui n’incorporent pas de profil de couleurs. Également pour les valeurs de couleur du RGB spécifiées avec diverses commandes de rendu d’image, telles que bgc= et color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 2%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Profil colorimétrique d’entrée par défaut du RGB. Indique le nom du profil de couleurs ICC à utiliser pour les images et les vignettes de matériaux RGB qui n’incorporent pas de profil de couleurs. Également pour les valeurs de couleur de RGB spécifiées avec diverses commandes de rendu d’image, telles que `bgc=` et `color=`.

## Propriétés {#section-c22966bba03e43c08e9d3fb91bfdd465}

Chaîne de texte. Si spécifié, doit être valide `icc::Name` de la carte de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou d’un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil de RGB.

## Par défaut {#section-0171cd6680284bfa9844b9cc3644ca61}

Hérité de `default::IccProfileSrcRgb` s’il n’est pas défini ou s’il est vide. If `attribute::IccProfileSrcRgb` ne se résout pas en un profil valide, `attribute::IccProfileRgb` est utilisée à la place.

## Voir aussi {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
