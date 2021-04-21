---
description: TTL de cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration des réponses d’image par défaut (réponses renvoyant une image par défaut spécifiée avec defaultImage= ou attribut DefaultImage).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# DefaultExpiration{#defaultexpiration}

TTL de cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration des réponses d’image par défaut (réponses renvoyant une image par défaut spécifiée avec defaultImage= ou attribute::DefaultImage).

Uniquement appliquée lorsque l’image par défaut n’est pas associée à un enregistrement de catalogue d’images ou lorsque l’enregistrement de catalogue d’images par défaut ne fournit pas de valeur `catalog::Expiration` spécifique.

## Propriétés {#section-e564512476604fd7b964f9f2903d6d33}

Nombre réel, 0 ou supérieur. Nombre d&#39;heures avant expiration depuis la génération des données de réponse. La valeur 0 permet de toujours faire expirer l’image de réponse immédiatement, ce qui désactive la mise en cache du client pour les réponses d’image par défaut. Définissez `-1` pour marquer comme `never expire`.

## Par défaut {#section-131cd32c2e214391857dba5af321f8cd}

Hérité de `default::DefaultExpiration` si elle n&#39;est pas définie ou si elle est vide.

TTL (durée de vie) est la durée avant l’expiration du cache. La durée de vie par défaut est de 1 heure.

## Voir aussi {#section-d8642c22e3d947129367dd76366963d6}

[catalogue ::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribut ::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
