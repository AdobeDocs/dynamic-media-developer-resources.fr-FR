---
description: Image de la réponse à une erreur. La diffusion d’images renvoie normalement un état d’erreur avec un message texte en cas d’erreur.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 1%

---


# ErrorImage{#errorimage}

Image de la réponse à une erreur. La diffusion d’images renvoie normalement un état d’erreur avec un message texte en cas d’erreur.

`attribute::ErrorImage` permet de configurer une image, une entrée de catalogue ou un modèle à renvoyer en cas d’erreur.

>[!NOTE]
>
>Les images manquantes peuvent également être gérées avec `attribute::DefaultImage`.

Un modèle de diffusion d’images peut être configuré pour afficher le texte du message d’erreur dans l’image de réponse. Les variables prédéfinies suivantes peuvent être incluses dans le modèle `$error.title`, qui est remplacé par une brève description de l&#39;erreur, et `$error.message`, qui est remplacé par une description plus détaillée de l&#39;erreur (le niveau de détail est configuré avec `attribute::ErrorDetail`).

L’état HTTP 200 est renvoyé si l’image/le modèle d’erreur peut être traité avec succès. Si une erreur se produit pendant ce traitement, l’état d’erreur HTTP et un message texte sont renvoyés.

## Propriétés {#section-f460c6c2dd1f46b29f9a79b093575f45}

Chaîne de texte. Si spécifié, doit être une valeur catalog::Id valide dans un catalogue d’images ou un chemin d’accès relatif (à `attribute::RootPath`) ou absolu à un fichier d’image accessible par le serveur d’images.

## Par défaut {#section-2885f289e5714ddca665a6aee401967f}

Hérité de `default::ErrorImage` si elle n&#39;est pas définie. Si défini mais vide, le comportement de l&#39;image d&#39;erreur est désactivé, même si `default::ErrorImage` est défini, et un état d&#39;erreur HTTP et un message texte sont renvoyés.

## Exemple {#section-c92090abe1d247529542a8dd4960c2e6}

Pour obtenir des images de réponse avec le message d’erreur généré dans l’image, nous devons d’abord définir le modèle dans le catalogue d’images. Dans ce cas, nous créons une entrée dans notre catalogue d’images appelée `onError`, contenant les éléments suivants dans `catalog::Modifier` :

`size=300,300&bgc=ffffff&text=$error.message$`

Le modèle est enregistré avec `attribute::ErrorImage` :

`ErrorImage=myCatalog/onError`

Dans cet exemple, le texte sera rendu à l’aide de la police par défaut, de la couleur de la police et de la taille de la police.

## Voir aussi {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribut ::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catalogue::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribut::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribut::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
