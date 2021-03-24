---
description: Stratégie de validation du cache du serveur. Indique quand les entrées de cache côté serveur sont validées.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Stratégie de validation du cache du serveur. Indique quand les entrées de cache côté serveur sont validées.

Avec la validation basée sur l’expiration, les documents source et les vignettes sont périodiquement contrôlés pour vérifier s’ils ont changé. Avec la validation basée sur un catalogue, les images source ne sont vérifiées qu’après modification de la valeur `catalog::TimeStamp`.

La validation basée sur un catalogue est recommandée lorsque des catalogues de vignettes et de matériaux sont utilisés. La validation basée sur l’expiration doit être utilisée lorsque les vignettes sont référencées dans les demandes de rendu d’image directement par chemin d’accès.

## Propriétés {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 pour sélectionner la validation basée sur l’expiration. 1 pour sélectionner la validation du cache basée sur un catalogue.

## Par défaut {#section-e09f3af8b6b3497d963199988dc5345d}

Hérité de `default::CacheValidationPolicy` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalogue ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
