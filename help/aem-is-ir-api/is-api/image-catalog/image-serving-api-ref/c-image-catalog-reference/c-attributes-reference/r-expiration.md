---
description: Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait pas de valeur d’expiration de catalogue valide.
seo-description: Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait pas de valeur d’expiration de catalogue valide.
seo-title: Expiration
solution: Experience Manager
title: Expiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Expiration{#expiration}

Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue spécifique ne contiendrait pas une valeur catalog::Expiration valide.

## Propriétés {#section-063be3b2f13a48a3a5ab8080718e9812}

Nombre réel, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez cette valeur sur 0 pour que l’image de réponse arrive à expiration immédiatement, ce qui désactive la mise en cache du client. Définissez sur -1 pour marquer comme `never expire`.

## Par défaut {#section-f55308b195c04083996f6717c8537634}

Héritée de `default::Expiration` si non définie ou si vide.

TTL (durée de vie) est la durée avant l’expiration du cache. La durée de vie par défaut est de 10 heures.

## Voir aussi {#section-b2411d99ddb14115ad475d506efd8967}

[catalogue::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribut::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribut::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
