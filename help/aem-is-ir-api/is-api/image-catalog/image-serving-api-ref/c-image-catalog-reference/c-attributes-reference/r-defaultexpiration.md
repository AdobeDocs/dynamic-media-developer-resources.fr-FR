---
description: Délai d’activation du cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration pour les réponses d’image par défaut (réponses qui renvoient une image par défaut spécifiée avec defaultImage= ou attribute DefaultImage).
solution: Experience Manager
title: Délai d’expiration par défaut
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---

# Délai d’expiration par défaut{#defaultexpiration}

Délai d’activation du cache client pour les réponses d’image par défaut. Fournit l’intervalle d’expiration des réponses d’image par défaut (réponses qui renvoient une image par défaut spécifiée avec defaultImage= ou attribute ::D efaultImage).

Appliquée uniquement lorsque l’image par défaut n’est pas associée à un enregistrement de catalogue ou lorsque l’enregistrement de catalogue d’images par défaut ne fournit pas de valeur spécifique `catalog::Expiration` .

## Propriétés {#section-e564512476604fd7b964f9f2903d6d33}

Nombre réel, supérieur ou égal à zéro. Nombre d’heures avant expiration depuis que les données de réponse ont été générées. Définissez sur 0 pour toujours faire expirer l’image de réponse immédiatement, ce qui désactive efficacement la mise en cache du client pour les réponses d’image par défaut. Définissez sur `-1` pour marquer comme `never expire`.

## Par défaut {#section-131cd32c2e214391857dba5af321f8cd}

Hérité de `default::DefaultExpiration` si non défini ou si vide.

TTL (Time-To-Live) est la durée avant l’expiration du cache. La durée de vie par défaut est de 1 heure.

## Voir aussi {#section-d8642c22e3d947129367dd76366963d6}

[catalog ::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribut ::D efaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
