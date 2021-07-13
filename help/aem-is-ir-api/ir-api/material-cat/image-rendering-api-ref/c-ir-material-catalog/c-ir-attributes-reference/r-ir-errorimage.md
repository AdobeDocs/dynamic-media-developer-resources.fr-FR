---
description: Image de réponse à une erreur. Le rendu d’image renvoie normalement un état d’erreur avec un message texte lorsqu’une erreur se produit. L’attribut ErrorImage permet de configurer une image à renvoyer en cas d’erreur.
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# ErrorImage *{#errorimage}

Image de réponse à une erreur. Le rendu d’image renvoie normalement un état d’erreur avec un message texte lorsqu’une erreur se produit. attribute::ErrorImage permet de configurer une image à renvoyer en cas d’erreur.

Lorsqu’une erreur se produit, le serveur tente pour la première fois d’interpréter la valeur de `ImageRendering::attribute::ErrorImage`comme un simple chemin d’accès au fichier image. Si le fichier ne peut pas être ouvert, il envoie la valeur d’attribut et les détails d’erreur à Image Serving, qui traite comme décrit dans la section `ImageServing::attribute::ErrorImage`. Si le serveur d’images ne renvoie pas d’image de réponse valide, l’état d’erreur HTTP standard et le message texte sont envoyés au client.

Les images d’erreur sont renvoyées avec l’état HTTP 200.

## Propriétés {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Chaîne de texte. S’il est spécifié, il doit s’agir d’une valeur **`ImageServing::catalog::id`**, d’un chemin relatif (à **`ImageServing::attribute::RootPath`** ou **`ImageRendering::attribute::RootPath`**) ou d’un chemin absolu vers un fichier image accessible par le serveur d’images.

## Par défaut {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Hérité de `default::ErrorImage` si elle n’est pas définie. Si elle est définie, mais vide, le comportement de l’image d’erreur est désactivé, même si `default::ErrorImage` est défini et un état d’erreur HTTP est renvoyé.

## Voir aussi {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
