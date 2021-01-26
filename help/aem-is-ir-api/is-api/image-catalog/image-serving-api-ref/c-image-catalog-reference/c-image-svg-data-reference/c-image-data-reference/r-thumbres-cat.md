---
description: Résolution des miniatures. Indique la résolution d’objet de l’image miniature.
seo-description: Résolution des miniatures. Indique la résolution d’objet de l’image miniature.
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10bbad31-a0fd-4ed3-b708-87822777acdd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# ThumbRes{#thumbres}

Résolution des miniatures. Indique la résolution d’objet de l’image miniature.

Utilisé uniquement si `catalog::ThumbType=3`.

## Propriétés {#section-ee5cae086a3d4875805fa8a08756a586}

Valeur du nombre réel supérieure à 0. Doit avoir les mêmes unités que `catalog::Resolution`.

## Par défaut {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` est utilisée si le champ n’est pas présent, si la valeur est 0 ou si le champ est vide.

## Voir aussi {#section-eb716bf647614db083020fe8ce453751}

[catalogue:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [catalogue::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [attribut::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Mise à l’échelle des miniatures](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)[
