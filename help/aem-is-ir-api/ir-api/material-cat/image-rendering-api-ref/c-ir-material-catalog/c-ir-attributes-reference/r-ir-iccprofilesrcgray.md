---
title: IccProfileSrcGray
description: Profil de couleurs d’entrée par défaut en niveaux de gris. Spécifie le nom du profil de couleurs ICC à utiliser pour les images de matériaux en niveaux de gris qui n’incorporent pas de profil de couleurs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Profil de couleurs d’entrée par défaut en niveaux de gris. Spécifie le nom du profil de couleurs ICC à utiliser pour les images de matériaux en niveaux de gris qui n’incorporent pas de profil de couleurs.

## Propriétés {#section-97923d8561b845309442d57d017d91a4}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant de la carte de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil en niveaux de gris.

## Par défaut {#section-02c52805ee13483dba7878aeab51f889}

Hérité de `default::IccProfileSrcGray` si elle n’est pas définie ou si elle est vide. Si `attribute::IccProfileSrcGray` ne se résout pas en un profil valide, `attribute::IccProfileGray` est utilisé à la place.

## Voir aussi {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
