---
description: Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue particulier ne contiendrait pas de valeur d’expiration de catalogue valide.
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 4%

---

# Expiration{#expiration}

Durée de vie par défaut du cache client. Fournit un intervalle d’expiration par défaut au cas où un enregistrement de catalogue particulier ne contiendrait pas de valeur catalog::Expiration valide.

## Propriétés {#section-063be3b2f13a48a3a5ab8080718e9812}

Nombre réel, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez cette variable sur 0 pour que l’image de réponse expire immédiatement, ce qui désactive la mise en cache du client. Définissez cette variable sur -1 pour marquer comme `never expire`.

## Par défaut {#section-f55308b195c04083996f6717c8537634}

Hérité de `default::Expiration` si elle n’est pas définie ou si elle est vide.

La durée de vie (TTL) est la durée avant l’expiration du cache. La durée de vie par défaut est de 10 heures.

## Voir aussi {#section-b2411d99ddb14115ad475d506efd8967}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
