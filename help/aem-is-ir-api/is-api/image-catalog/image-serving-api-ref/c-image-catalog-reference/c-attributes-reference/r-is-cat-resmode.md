---
title: ResMode
description: Mode de rééchantillonnage par défaut. Indique les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour le dimensionnement des données d’image.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# ResMode{#resmode}

Mode de rééchantillonnage par défaut. Indique les attributs de rééchantillonnage et d’interpolation par défaut à utiliser pour le dimensionnement des données d’image.

Utilisé lorsque `resMode=` n’est pas spécifié dans une requête.

## Propriétés {#section-493f900be522486f97710cebdc4460c2}

Enum. Définissez cette variable sur 2 pour `bilin`, 3 pour `bicub` ou 4 pour le mode d’interpolation `sharp2` (voir [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) pour plus d’informations). `sharp` (1) est en cours d’obsolescence. Utilisez `sharp2` (4) à la place pour obtenir les meilleurs résultats.

## Par défaut {#section-35f980e745fc4d79a2621e8abacc724d}

Hérité de `default::ResMode` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
