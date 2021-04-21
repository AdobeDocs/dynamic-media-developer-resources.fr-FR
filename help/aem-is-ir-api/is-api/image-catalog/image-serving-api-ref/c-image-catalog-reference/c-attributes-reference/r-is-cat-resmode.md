---
description: Mode de rééchantillonnage par défaut. Indique les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour la mise à l’échelle des données d’image.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

---


# ResMode{#resmode}

Mode de rééchantillonnage par défaut. Indique les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour la mise à l’échelle des données d’image.

Utilisé lorsque `resMode=` n&#39;est pas spécifié dans une requête.

## Propriétés {#section-493f900be522486f97710cebdc4460c2}

Enum. Définissez sur 2 pour `bilin`, 3 pour `bicub` ou 4 pour le mode d&#39;interpolation `sharp2` (voir ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` pour plus de détails). `sharp` (1) est en cours de désapprobation. Utilisez `sharp2` (4) à la place pour obtenir de meilleurs résultats.

## Par défaut {#section-35f980e745fc4d79a2621e8abacc724d}

Hérité de `default::ResMode` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
