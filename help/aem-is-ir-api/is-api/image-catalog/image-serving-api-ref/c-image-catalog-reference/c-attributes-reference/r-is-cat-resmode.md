---
description: Mode de rééchantillonnage par défaut. Indique les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour le dimensionnement des données d’image.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

Mode de rééchantillonnage par défaut. Indique les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour le dimensionnement des données d’image.

Utilisé lorsque `resMode=` n’est pas spécifié dans une requête.

## Propriétés {#section-493f900be522486f97710cebdc4460c2}

Enum. Définissez cette variable sur 2 pour `bilin`, 3 pour `bicub` ou 4 pour le mode d’interpolation `sharp2` (voir ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` pour plus de détails). `sharp` (1) est en cours d’abandon. Utilisez `sharp2` (4) à la place pour obtenir les meilleurs résultats.

## Par défaut {#section-35f980e745fc4d79a2621e8abacc724d}

Hérité de `default::ResMode` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
