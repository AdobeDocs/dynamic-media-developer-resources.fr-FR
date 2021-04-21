---
description: Temps de mise en cache du client par défaut à vivre. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait pas de valeur d’expiration de catalogue valide.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 4%

---


# Expiration{#expiration}

Temps de mise en cache du client par défaut à vivre. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait pas de valeur catalog::Expiration valide.

## Propriétés {#section-063be3b2f13a48a3a5ab8080718e9812}

Nombre réel, 0 ou supérieur. Nombre d&#39;heures avant expiration depuis la génération des données de réponse. La valeur 0 permet de toujours faire expirer l’image de réponse immédiatement, ce qui désactive la mise en cache du client. Définissez sur -1 pour marquer comme `never expire`.

## Par défaut {#section-f55308b195c04083996f6717c8537634}

Hérité de `default::Expiration` si elle n&#39;est pas définie ou si elle est vide.

TTL (durée de vie) est la durée avant l’expiration du cache. La durée de vie par défaut est de 10 heures.

## Voir aussi {#section-b2411d99ddb14115ad475d506efd8967}

[catalogue ::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribut ::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribut ::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
