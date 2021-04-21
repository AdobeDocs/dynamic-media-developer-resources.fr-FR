---
description: Expiration
solution: Experience Manager
title: Expiration
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 2%

---


# Expiration{#expiration}

Permet de gérer la mise en cache du client et du serveur proxy. Le serveur calcule la date/l’heure d’expiration des données de réponse HTTP en ajoutant cette valeur à l’heure/la date de transmission.

Les navigateurs gèrent les caches à l’aide des heures d’expiration des fichiers. Avant de transmettre une requête au serveur, le navigateur vérifie son cache pour vérifier si le fichier a déjà été téléchargé. Si tel est le cas, et si le fichier n’a pas encore expiré, le navigateur envoie une requête de GET conditionnelle (par exemple avec le champ If-Modified-Since défini dans l’en-tête de la requête) plutôt qu’une requête de GET normale. Le serveur a la possibilité de répondre avec un état &quot;304&quot; et de ne pas transmettre l’image. Le navigateur charge ensuite le fichier à partir de son cache. Cela peut considérablement augmenter les performances globales pour les données fréquemment consultées.

L’expiration est utilisée pour les types de réponse suivants :

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Certains types de réponses (par exemple, les réponses d&#39;erreur) sont toujours marqués pour une expiration immédiate (ou marqués comme non pouvant être mis en cache), tandis que d&#39;autres (par exemple, les réponses de propriété ou d&#39;image par défaut) utilisent des paramètres d&#39;expiration spéciaux ( `attribute::NonImgExpiration` et `attribute::DefaultExpiration`).

## Propriétés {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Nombre réel, -2, -1 ou 0 ou plus. Nombre d’heures avant expiration depuis la génération de l’image de réponse. La valeur 0 permet de toujours faire expirer l’image de réponse immédiatement, ce qui désactive la mise en cache du client. Définissez sur -1 pour marquer comme *`never expire`*. Dans ce cas, le serveur renvoie toujours l’état 304 (non modifié) en réponse à des demandes de GET conditionnelles sans vérifier si le fichier a réellement changé. Définissez cette variable sur -2 pour utiliser la valeur par défaut fournie par `attribute::Expiration`.

## Par défaut {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` est utilisée si le champ n’est pas présent, si la valeur est -2 ou si le champ est vide.

## Voir aussi {#section-0e5e8595aad641c689726828712a8902}

[attribut::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [attribut::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [attribut::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
