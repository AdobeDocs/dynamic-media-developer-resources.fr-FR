---
description: de couleur d’entrée par défaut en niveaux de gris. Indique le nom du de couleurs ICC à utiliser pour les images de matériau en niveaux de gris qui n’incorporent pas de de couleur .
seo-description: de couleur d’entrée par défaut en niveaux de gris. Indique le nom du de couleurs ICC à utiliser pour les images de matériau en niveaux de gris qui n’incorporent pas de de couleur .
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcGray{#iccprofilesrcgray}

de couleur d’entrée par défaut en niveaux de gris. Indique le nom du de couleurs ICC à utiliser pour les images de matériau en niveaux de gris qui n’incorporent pas de de couleur .

## Propriétés {#section-97923d8561b845309442d57d017d91a4}

Chaîne de texte. Le cas échéant, doit correspondre à une `icc::Name` valeur valide de la carte de  ICC de ce catalogue d’images ou du catalogue par défaut, ou à un chemin d’accès de fichier relatif à `attribute::RootPath`. Le  ICC référencé doit être un en niveaux de gris.

## Par défaut {#section-02c52805ee13483dba7878aeab51f889}

Héritée de `default::IccProfileSrcGray` si non définie ou si vide. Si `attribute::IccProfileSrcGray` la résolution ne correspond pas à un  valide, `attribute::IccProfileGray` sera utilisé à la place.

## Voir aussi {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribut::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribut::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribut::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
