---
description: Durée de vie du cache client pour les réponses non-images. Fournit l’intervalle d’expiration de certaines réponses non images.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---

# NonImgExpiration{#nonimgexpiration}

Durée de vie du cache client pour les réponses non-images. Fournit l’intervalle d’expiration de certaines réponses non images.

Fournit l’intervalle d’expiration de certaines réponses autres que des images, y compris celles envoyées en réponse aux commandes suivantes :

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Propriétés {#section-d37e3113f4b1468b86b5a14e80d94c83}

Nombre réel, 0 ou supérieur. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez cette variable sur 0 pour que l’image de réponse expire toujours immédiatement, ce qui désactive la mise en cache du client pour les réponses d’image par défaut. Définissez cette variable sur -1 pour marquer comme *ne jamais expirer*.

## Par défaut {#section-96981360c0234b7f824d2ff7c25a7954}

Hérité de `default::NonImgExpiration` si elle n’est pas définie ou si elle est vide.

La durée de vie (TTL) est la durée avant l’expiration du cache. La durée de vie par défaut est de 6 minutes.

## Voir aussi {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalogue ::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribut::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
