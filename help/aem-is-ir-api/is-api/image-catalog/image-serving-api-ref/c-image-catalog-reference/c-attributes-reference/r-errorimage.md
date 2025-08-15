---
description: Image de réponse d’erreur. La diffusion d’images renvoie normalement un statut d’erreur avec un message texte lorsqu’une erreur se produit.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# ErrorImage{#errorimage}

Image de réponse d’erreur. La diffusion d’images renvoie normalement un statut d’erreur avec un message texte lorsqu’une erreur se produit.

`attribute::ErrorImage` permet de configurer le renvoi d’une image, d’une entrée de catalogue ou d’un modèle en cas d’erreur.

>[!NOTE]
>
>Les images manquantes peuvent également être gérées avec `attribute::DefaultImage`.

Un modèle de diffusion d’images peut être configuré afin d’effectuer le rendu du texte du message d’erreur dans l’image de réponse. Les variables prédéfinies suivantes peuvent être incluses dans le modèle de `$error.title`, qui est remplacé par une brève description d’erreur, et `$error.message`, qui est remplacé par une description d’erreur plus détaillée (le niveau de détail est configuré avec `attribute::ErrorDetail`).

Le statut HTTP 200 est renvoyé si l’image/le modèle d’erreur peut être traité avec succès. Si une erreur se produit lors de ce traitement, le statut d’erreur HTTP et un message texte sont renvoyés.

## Propriétés {#section-f460c6c2dd1f46b29f9a79b093575f45}

Chaîne de texte. Si spécifié, doit être une valeur catalog::Id valide dans un catalogue d’images ou un chemin relatif (vers `attribute::RootPath`) ou absolu vers un fichier image accessible par le serveur d’images.

## Par défaut {#section-2885f289e5714ddca665a6aee401967f}

Hérité de `default::ErrorImage` si non défini. Si défini mais vide, le comportement de l’image d’erreur est désactivé, même si `default::ErrorImage` est défini, et un statut d’erreur HTTP et un message texte sont renvoyés.

## Exemple {#section-c92090abe1d247529542a8dd4960c2e6}

Pour obtenir des images de réponse avec le message d’erreur rendu dans l’image, nous devons d’abord définir le modèle dans le catalogue d’images. Dans ce cas, nous créons une entrée dans notre catalogue d’images, appelée `onError`, contenant les éléments suivants en `catalog::Modifier` :

`size=300,300&bgc=ffffff&text=$error.message$`

Le modèle est enregistré auprès de `attribute::ErrorImage` :

`ErrorImage=myCatalog/onError`

Dans cet exemple, le texte est rendu à l’aide de la police par défaut, de sa couleur et de sa taille.

## Voir aussi {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
