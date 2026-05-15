---
description: TTL de cache client pour les réponses autres que les images. Fournit l’intervalle d’expiration pour certaines réponses autres que des images.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
TQID: 'https://experienceleague.adobe.com/A21KkwsYFIMp9Pw0WyX-c-3UVlFg2FacObh2jjRVTwA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 2%

---

# NonImgExpiration{#nonimgexpiration}

TTL de cache client pour les réponses autres que les images. Fournit l’intervalle d’expiration pour certaines réponses autres que des images.

Fournit l’intervalle d’expiration pour certaines réponses autres que les images, y compris celles envoyées en réponse aux commandes suivantes :

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Propriétés {#section-d37e3113f4b1468b86b5a14e80d94c83}

Nombre réel, supérieur ou égal à 0. Nombre d’heures avant expiration depuis la génération des données de réponse. Définissez la valeur sur 0 pour que l’image de réponse expire immédiatement, ce qui désactive la mise en cache du client pour les réponses d’image par défaut. Définissez sur -1 pour marquer comme *n’expire jamais*.

## Par défaut {#section-96981360c0234b7f824d2ff7c25a7954}

Hérité de `default::NonImgExpiration` si non défini ou si vide.

La durée de vie (TTL) correspond à la durée avant l’expiration du cache. La durée de vie par défaut est de 6 minutes.

## Voir aussi {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
