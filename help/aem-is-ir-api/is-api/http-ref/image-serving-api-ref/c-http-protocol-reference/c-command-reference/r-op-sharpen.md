---
title: op_sharpen
description: Accentuer l’image. Applique un filtre d’accentuation de base au calque ou à l’image de la vue finale, après toute mise à l’échelle, si layer=comp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 62e7d91c-935f-410f-a971-ffb3cfff31d6
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 6%

---

# op_sharpen{#op-sharpen}

Accentuer l’image. Applique un filtre d’accentuation de base au calque ou à l’image de la vue finale, après toute mise à l’échelle, si layer=comp.

`op_sharpen=0|1`

Le masque de calque ou le masque composite est également accentué.

## Propriétés {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Attribut de calque ou attribut d’affichage. S’applique au calque actif ou à l’image d’affichage final si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, sans effet d’accentuation.

## Exemple {#section-3202122df5db4e14b358ecabfb6d8b85}

Compenser le léger flou causé par le rééchantillonnage d’images. Nous augmentons également la qualité du JPEG afin d’éviter des artefacts de JPEG supplémentaires le long des bords accentués.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Voir aussi {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
