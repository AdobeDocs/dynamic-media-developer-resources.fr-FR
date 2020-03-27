---
description: Image de la réponse à l’erreur. Le rendu d’image renvoie normalement un état d’erreur avec un message texte en cas d’erreur. L’attribut ErrorImage permet de configurer une image à renvoyer en cas d’erreur.
seo-description: Image de la réponse à l’erreur. Le rendu d’image renvoie normalement un état d’erreur avec un message texte en cas d’erreur. L’attribut ErrorImage permet de configurer une image à renvoyer en cas d’erreur.
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorImage *{#errorimage}

Image de la réponse à l’erreur. Le rendu d’image renvoie normalement un état d’erreur avec un message texte en cas d’erreur. attribute::ErrorImage permet de configurer une image à renvoyer en cas d&#39;erreur.

Lorsqu’une erreur se produit, le serveur tente tout d’abord d’interpréter la valeur de `ImageRendering::attribute::ErrorImage`comme un simple chemin d’accès au fichier image. Si le fichier ne peut pas être ouvert, il envoie la valeur d’attribut et les détails d’erreur à Image Serving, qui traite comme décrit dans `ImageServing::attribute::ErrorImage`. Si Image Serving ne renvoie pas d’image de réponse valide, l’état d’erreur HTTP standard et le message texte sont envoyés au client.

Les images d’erreur sont renvoyées avec l’état HTTP 200.

## Propriétés {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Chaîne de texte. S’il est spécifié, il doit s’agir d’une **`ImageServing::catalog::id`** valeur, d’un chemin relatif (vers **`ImageServing::attribute::RootPath`** ou **`ImageRendering::attribute::RootPath`**) ou d’un chemin absolu vers un fichier image accessible par le serveur d’images.

## Par défaut {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Hérité de `default::ErrorImage` si elle n’est pas définie. Si elle est définie mais vide, le comportement de l’image d’erreur est désactivé, même si `default::ErrorImage` est défini, et un état d’erreur HTTP est renvoyé.

## Voir aussi {#section-3e0308eaf4124451909dacd570e27695}

[attribut::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribut::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribut::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalogue::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
