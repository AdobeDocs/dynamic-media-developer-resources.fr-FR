---
description: Taille limite de l’image de réponse. Largeur et hauteur maximales de l’image de réponse qui peuvent être renvoyées au client.
seo-description: Taille limite de l’image de réponse. Largeur et hauteur maximales de l’image de réponse qui peuvent être renvoyées au client.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# MaxPix{#maxpix}

Taille limite de l’image de réponse. Largeur et hauteur maximales de l’image de réponse qui peuvent être renvoyées au client.

Le serveur renvoie une erreur si une requête provoque une image de réponse dont la largeur et/ou la hauteur sont supérieures à `attribute::MaxSize`.

## Propriétés {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Deux nombres entiers, supérieurs à 0, séparés par une virgule. Largeur et hauteur en pixels. Peut également être défini sur 0,0 pour permettre toute taille d’image de réponse sans limite.

## Par défaut {#section-45b38dc661854d11b97df5709f4f3434}

Hérité de default::MaxPix si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
