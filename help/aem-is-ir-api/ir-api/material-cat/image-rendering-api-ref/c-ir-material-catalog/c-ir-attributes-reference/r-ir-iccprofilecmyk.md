---
title: IccProfileCmyk
description: Espace colorimétrique CMJN par défaut. Indique le nom du profil colorimétrique ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c36ea45d-dc91-4afa-825a-7af49738101c
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---

# IccProfileCmyk{#iccprofilecmyk}

Espace colorimétrique CMJN par défaut. Indique le nom du profil colorimétrique ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec `icc=`.

## Propriétés {#section-849678b272954bdcb236f49aa54f1609}

Chaîne de texte. Si spécifié, doit être une valeur de `icc::Name` valide de la carte de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès au fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-55026b7454af4d868bcb47f7743c9c5b}

Hérité de `default::IccProfileCmyk` si non défini ou si vide.

## Voir aussi {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
