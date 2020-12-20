---
description: Résolution. Résolution d’image "réelle", généralement exprimée en pixels par pouce, mais peut également se trouver dans d’autres unités, telles que les pixels par mètre.
seo-description: Résolution. Résolution d’image "réelle", généralement exprimée en pixels par pouce, mais peut également se trouver dans d’autres unités, telles que les pixels par mètre.
seo-title: Résolution
solution: Experience Manager
title: Résolution
topic: Scene7 Image Serving - Image Rendering API
uuid: 281c7ff6-8f78-4654-98ec-0db4299b80d9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 8%

---


# Résolution{#resolution}

Résolution. Résolution d’image &quot;réelle&quot;, généralement exprimée en pixels par pouce, mais peut également se trouver dans d’autres unités, telles que les pixels par mètre.

## Propriétés {#section-985ca2ad858c4e9c9cbb303f55447553}

Nombre réel, supérieur à 0. Requis pour les matériaux de texture et de décale, sauf si la résolution de l&#39;image est identique à attribut::Resolution. Ignoré par les matériaux de couleur unie et d&#39;armoire.

## Par défaut {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` est utilisée si le champ n’est pas présent, si la valeur est 0 ou négative ou si le champ est vide.

## Voir aussi {#section-2d04df523d7345f6929178cbc637da78}

[attribut ::Résolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
