---
title: IccProfileSrcCmyk
description: Profil colorimétrique d’entrée CMJN par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images en matériau CMJN qui n’incorporent pas de profil de couleurs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 2%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Profil colorimétrique d’entrée CMJN par défaut. Indique le nom du profil de couleurs ICC à utiliser pour les images en matériau CMJN qui n’incorporent pas de profil de couleurs.

## Propriétés {#section-0cee77438d914c319ec876edb3490821}

Chaîne de texte. Si spécifié, doit être une valeur de `icc::Name` valide de la carte de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-11f6239e0dd14827abf4a95c1b30161c}

Hérité de `default::IccProfileSrcCmyk` si non défini ou si vide. Si `attribute::IccProfileSrcCmyk` ne correspond pas à un profil valide, `attribute::IccProfileCmyk` est utilisé à la place.

## Voir aussi {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
