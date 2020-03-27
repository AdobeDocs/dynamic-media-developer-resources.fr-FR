---
description: Mode de rééchantillonnage par défaut. Spécifie les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour le redimensionnement des données d’image.
seo-description: Mode de rééchantillonnage par défaut. Spécifie les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour le redimensionnement des données d’image.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ResMode{#resmode}

Mode de rééchantillonnage par défaut. Spécifie les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour le redimensionnement des données d’image.

Utilisé lorsqu’ `resMode=` il n’est pas spécifié dans une requête.

## Propriétés {#section-493f900be522486f97710cebdc4460c2}

Enum. Définissez sur 2 pour `bilin`, 3 pour `bicub`ou 4 pour `sharp2` le mode d’interpolation (voir ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` pour plus de détails). `sharp` (1) est en cours de désapprobation. Utilisez `sharp2` (4) à la place pour obtenir de meilleurs résultats.

## Par défaut {#section-35f980e745fc4d79a2621e8abacc724d}

Héritée de `default::ResMode` si non définie ou si vide.

## Voir aussi {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
