---
description: TTL du cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration des réponses d’image par défaut (réponses renvoyant une image par défaut spécifiée avec defaultImage= ou attribut DefaultImage).
seo-description: TTL du cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration des réponses d’image par défaut (réponses renvoyant une image par défaut spécifiée avec defaultImage= ou attribut DefaultImage).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultExpiration{#defaultexpiration}

TTL du cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration des réponses d’image par défaut (réponses renvoyant une image par défaut spécifiée avec defaultImage= ou attribute::DefaultImage).

Uniquement appliquée lorsque l’image par défaut n’est pas associée à un enregistrement de catalogue d’images ou lorsque l’enregistrement de catalogue d’images par défaut ne fournit pas de `catalog::Expiration` valeur spécifique.

## Propriétés {#section-e564512476604fd7b964f9f2903d6d33}

Nombre réel, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez cette valeur sur 0 pour que l’image de réponse arrive à expiration immédiatement, ce qui désactive la mise en cache du client pour les réponses d’image par défaut. Définissez cette variable sur `-1` marquer comme `never expire`.

## Par défaut {#section-131cd32c2e214391857dba5af321f8cd}

Héritée de `default::DefaultExpiration` si non définie ou si vide.

TTL (durée de vie) est la durée avant l’expiration du cache. La durée de vie par défaut est de 1 heure.

## Voir aussi {#section-d8642c22e3d947129367dd76366963d6}

[catalogue::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribut::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
