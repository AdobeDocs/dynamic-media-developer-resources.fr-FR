---
description: Espace colorimétrique par défaut en niveaux de gris. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc=.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# IccProfileGray{#iccprofilegray}

Espace colorimétrique par défaut en niveaux de gris. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc=.

## Propriétés {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant de la carte de profil ICC de ce catalogue de matériaux ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil en niveaux de gris.

## Par défaut {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Hérité de `default::IccProfileGray` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
