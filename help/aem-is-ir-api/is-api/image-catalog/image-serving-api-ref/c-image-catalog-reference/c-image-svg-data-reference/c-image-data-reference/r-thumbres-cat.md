---
description: Résolution des miniatures. Indique la résolution d’objet de la miniature.
solution: Experience Manager
title: Pouces
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 4%

---

# Pouces{#thumbres}

Résolution des miniatures. Indique la résolution d’objet de la miniature.

Utilisée uniquement si `catalog::ThumbType=3`.

## Propriétés {#section-ee5cae086a3d4875805fa8a08756a586}

Valeur de nombre réel supérieure à 0. Doit avoir les mêmes unités que `catalog::Resolution`.

## Par défaut {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` est utilisée si le champ est absent, si la valeur est 0 ou si le champ est vide.

## Voir aussi {#section-eb716bf647614db083020fe8ce453751}

[:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) catalog , [catalog ::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [attribute ::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Mise à l’échelle des miniatures](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
