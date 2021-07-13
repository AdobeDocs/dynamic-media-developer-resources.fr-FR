---
description: Stratégie de validation du cache du serveur. Indique le moment où les entrées du cache côté serveur sont validées.
solution: Experience Manager
title: CacheValidationPolicy
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Stratégie de validation du cache du serveur. Indique le moment où les entrées du cache côté serveur sont validées.

Avec la validation basée sur l’expiration, les images sources sont régulièrement vérifiées si elles ont changé. Avec la validation basée sur un catalogue, les images sources ne sont vérifiées qu’après modification de la valeur `catalog::TimeStamp`.

La validation basée sur un catalogue est recommandée lorsque des catalogues d’images sont utilisés. La validation basée sur l’expiration doit être utilisée lorsque les images sont référencées directement, sans utiliser de catalogue d’images.

## Propriétés {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 pour sélectionner la validation basée sur l’expiration, 1 pour sélectionner la validation du cache basée sur le catalogue.

## Par défaut {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Hérité de `default::CacheValidationPolicy` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalogue ::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
