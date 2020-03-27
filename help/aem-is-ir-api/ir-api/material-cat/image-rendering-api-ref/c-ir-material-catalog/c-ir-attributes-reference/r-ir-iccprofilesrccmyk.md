---
description: de couleurs d’entrée CMJN par défaut. Indique le nom du de couleurs ICC à utiliser pour les images de matériau CMJN qui n’incorporent pas de de couleur .
seo-description: de couleurs d’entrée CMJN par défaut. Indique le nom du de couleurs ICC à utiliser pour les images de matériau CMJN qui n’incorporent pas de de couleur .
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: 95147b28-c87b-4337-a0eb-a962ca1e8786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

de couleurs d’entrée CMJN par défaut. Indique le nom du de couleurs ICC à utiliser pour les images de matériau CMJN qui n’incorporent pas de de couleur .

## Propriétés {#section-0cee77438d914c319ec876edb3490821}

Chaîne de texte. Le cas échéant, doit correspondre à une `icc::Name` valeur valide de la carte de  ICC de ce catalogue d’images ou du catalogue par défaut, ou à un chemin d’accès de fichier relatif à `attribute::RootPath`. Le ICC référencé doit être un CMJN .

## Par défaut {#section-11f6239e0dd14827abf4a95c1b30161c}

Héritée de `default::IccProfileSrcCmyk` si non définie ou si vide. Si `attribute::IccProfileSrcCmyk` la résolution ne correspond pas à un  valide, `attribute::IccProfileCmyk` sera utilisé à la place.

## Voir aussi {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribut::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribut::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [attribut::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
