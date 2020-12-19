---
description: TTL de cache client pour les réponses sans image. Fournit l’intervalle d’expiration pour certaines réponses autres que les images.
seo-description: TTL de cache client pour les réponses sans image. Fournit l’intervalle d’expiration pour certaines réponses autres que les images.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
topic: Scene7 Image Serving - Image Rendering API
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# NonImgExpiration{#nonimgexpiration}

TTL de cache client pour les réponses sans image. Fournit l’intervalle d’expiration pour certaines réponses autres que les images.

Fournit l’intervalle d’expiration de certaines réponses autres que les images, y compris celles envoyées en réponse aux commandes suivantes :

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Propriétés {#section-d37e3113f4b1468b86b5a14e80d94c83}

Nombre réel, 0 ou supérieur. Nombre d&#39;heures avant expiration depuis la génération des données de réponse. La valeur 0 permet de toujours faire expirer l’image de réponse immédiatement, ce qui désactive la mise en cache du client pour les réponses d’image par défaut. Définissez sur -1 pour marquer comme *n’expire jamais*.

## Par défaut {#section-96981360c0234b7f824d2ff7c25a7954}

Hérité de `default::NonImgExpiration` si elle n&#39;est pas définie ou si elle est vide.

TTL (durée de vie) est la durée avant l’expiration du cache. La durée de vie par défaut est de 6 minutes.

## Voir aussi {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalogue ::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribut ::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
