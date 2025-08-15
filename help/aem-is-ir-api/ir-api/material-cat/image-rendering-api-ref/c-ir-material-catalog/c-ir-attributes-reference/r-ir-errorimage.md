---
title: Image erronée
description: Image de réponse d’erreur. Image Rendering renvoie normalement un état d’erreur avec un message texte lorsqu’une erreur se produit.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---

# Image erronée {#errorimage}

Image de réponse d’erreur. Image Rendering renvoie normalement un état d’erreur avec un message texte lorsqu’une erreur se produit. Le `attribute::ErrorImage` permet de configurer une image à renvoyer en cas d’erreur.

Lorsqu’une erreur se produit, le serveur tente d’interpréter la valeur de comme un simple chemin d’accès `ImageRendering::attribute::ErrorImage`au fichier image. Si le fichier ne peut pas être ouvert, il envoie la valeur d’attribut et les détails de l’erreur au serveur d’images, qui traite comme décrit dans `ImageServing::attribute::ErrorImage`. Si la diffusion d’images ne renvoie pas d’image de réponse valide, l’état d’erreur HTTP standard et le message texte sont envoyés au client.

Les images d’erreur sont renvoyées avec l’état HTTP 200.

## Propriétés {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Chaîne de texte. S’il est spécifié, il doit s’agir d’une **`ImageServing::catalog::id`** valeur, d’un chemin d’accès relatif (vers **`ImageServing::attribute::RootPath`** ou ) **`ImageRendering::attribute::RootPath`** ou d’un chemin d’accès absolu à un fichier image accessible par le serveur d’images.

## Par défaut {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Hérité de `default::ErrorImage` si elle n’est pas définie. Si elle est définie mais vide, le comportement d’image d’erreur est désactivé, même s’il `default::ErrorImage` est défini, et un état d’erreur HTTP est renvoyé.

## Voir aussi {#section-3e0308eaf4124451909dacd570e27695}

[attribute ::D efaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute ::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute ::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog ::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
