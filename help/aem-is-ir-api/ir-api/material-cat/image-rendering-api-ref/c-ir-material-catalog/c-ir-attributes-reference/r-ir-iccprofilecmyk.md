---
description: Espace colorimétrique par défaut CMJN. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc=.
seo-description: Espace colorimétrique par défaut CMJN. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc=.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 2%

---


# IccProfileCmyk{#iccprofilecmyk}

Espace colorimétrique par défaut CMJN. Indique le nom du profil de couleurs ICC à utiliser pour les images de réponse en niveaux de gris lorsqu’aucun espace colorimétrique de sortie n’est spécifié avec icc=.

## Propriétés {#section-849678b272954bdcb236f49aa54f1609}

Chaîne de texte. Si spécifié, doit être une valeur `icc::Name` valide provenant du mappage de profil ICC de ce catalogue d’images ou du catalogue par défaut, ou un chemin d’accès de fichier relatif à `attribute::RootPath`. Le profil ICC référencé doit être un profil CMJN.

## Par défaut {#section-55026b7454af4d868bcb47f7743c9c5b}

Hérité de `default::IccProfileCmyk` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
