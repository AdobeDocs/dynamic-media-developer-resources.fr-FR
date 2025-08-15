---
title: Mode ResMode
description: Mode de rééchantillonnage par défaut. Spécifie les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour la mise à l’échelle des données d’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# Mode ResMode{#resmode}

Mode de rééchantillonnage par défaut. Spécifie les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour la mise à l’échelle des données d’image.

Utilisé quand `resMode=` n’est pas indiqué dans une requête.

## Propriétés {#section-493f900be522486f97710cebdc4460c2}

Enum. Définissez sur 2 pour `bilin`, 3 pour `bicub`et 4 pour `sharp2` le mode d’interpolation (voir [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) pour plus de détails). `sharp` (1) est en passe d’être désapprouvée. Utilisez `sharp2` (4) à la place pour de meilleurs résultats.

## Par défaut {#section-35f980e745fc4d79a2621e8abacc724d}

Hérité de `default::ResMode` si non défini ou si vide.

## Voir aussi {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
