---
description: Accentuer l’image. Applique un filtre d’accentuation de base au calque ou à l’image de vue finale, après mise à l’échelle, si layer=comp.
solution: Experience Manager
title: op_sharpen
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 7%

---


# op_sharpen{#op-sharpen}

Accentuer l’image. Applique un filtre d’accentuation de base au calque ou à l’image de vue finale, après mise à l’échelle, si layer=comp.

`op_sharpen=0|1`

Le masque de calque ou le masque composite est également accentué.

## Propriétés {#section-b27f3f6a27c34233b3f76805e18b2aa7}

Attribut de couche ou attribut de vue. S’applique au calque actif ou à l’image de vue finale si `layer=comp`. Ignoré par les calques d’effet.

## Par défaut {#section-665709700fff458e9dbbf8a78e8ecf71}

`op_sharpen=0`, sans effet d’accentuation.

## Exemple {#section-3202122df5db4e14b358ecabfb6d8b85}

Compenser le léger flou provoqué par le rééchantillonnage d’images. Nous augmentons également la qualité JPEG pour éviter d’autres artefacts JPEG le long des bords accentués.

`http://server/myRootId/myImageId?qlt=90,1&op_sharpen=1&wid=500`

## Voir aussi {#section-d659199fde0d4c9dadebf1f09802915d}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [op_usm=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-sharpen.md#reference-c32573230c6140f883efdaa201ea8541)
