---
description: Stratégie de validation du cache du serveur. Indique le moment où les entrées du cache côté serveur sont validées.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Stratégie de validation du cache du serveur. Indique le moment où les entrées du cache côté serveur sont validées.

La validation basée sur l’expiration permet de vérifier régulièrement les documents sources et les vignettes afin de vérifier s’ils ont changé. Avec la validation basée sur un catalogue, les images sources ne sont vérifiées qu’après modification de la valeur `catalog::TimeStamp`.

La validation basée sur un catalogue est recommandée lorsque des catalogues de documents et de vignettes sont utilisés. La validation basée sur l’expiration doit être utilisée lorsque les vignettes sont référencées dans les demandes de rendu d’image directement par le chemin d’accès.

## Propriétés {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 pour sélectionner la validation basée sur l’expiration. 1 pour sélectionner la validation du cache basée sur le catalogue.

## Par défaut {#section-e09f3af8b6b3497d963199988dc5345d}

Hérité de `default::CacheValidationPolicy` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-b374e4d908e24af8995b2b376ca1be8b}

[catalogue ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
