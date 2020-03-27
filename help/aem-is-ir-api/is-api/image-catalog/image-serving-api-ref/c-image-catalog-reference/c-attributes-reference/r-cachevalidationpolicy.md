---
description: Stratégie de validation du cache du serveur. Indique le moment où les entrées de cache côté serveur sont validées.
seo-description: Stratégie de validation du cache du serveur. Indique le moment où les entrées de cache côté serveur sont validées.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Scene7 Image Serving - Image Rendering API
uuid: 371dadbf-d58e-4214-8050-7e8907b436e3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CacheValidationPolicy{#cachevalidationpolicy}

Stratégie de validation du cache du serveur. Indique le moment où les entrées de cache côté serveur sont validées.

Avec la validation basée sur l’expiration, les images source sont périodiquement vérifiées pour vérifier si elles ont été modifiées. Avec la validation basée sur un catalogue, les images source ne sont vérifiées qu’une fois la `catalog::TimeStamp` valeur modifiée.

La validation basée sur un catalogue est recommandée lorsque des catalogues d’images sont utilisés. La validation basée sur l’expiration doit être utilisée lorsque les images sont référencées directement, sans l’utilisation d’un catalogue d’images.

## Propriétés {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 pour sélectionner la validation basée sur l’expiration, 1 pour sélectionner la validation du cache basée sur le catalogue.

## Par défaut {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Héritée de `default::CacheValidationPolicy` si non définie ou si vide.

## Voir aussi {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catalogue::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
