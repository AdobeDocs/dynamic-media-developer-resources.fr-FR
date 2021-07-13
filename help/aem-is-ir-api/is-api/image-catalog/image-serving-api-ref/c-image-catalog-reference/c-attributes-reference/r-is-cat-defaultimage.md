---
description: Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser si un fichier image est introuvable et que defaultImage= n’est pas spécifié dans la requête.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---

# DefaultImage{#defaultimage}

Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser si un fichier image est introuvable et que defaultImage= n’est pas spécifié dans la requête.

Il peut s’agir d’une entrée de catalogue (y compris un modèle) ou d’un chemin d’accès relatif (à `attribute::RootPath`) ou absolu au fichier image. Utile pour remplacer les images manquantes par des images par défaut.

## Propriétés {#section-b6d8193827c34e5f948792aba8b8daaf}

Chaîne de texte. Si spécifié, doit être une valeur `catalog::Id` valide dans ce catalogue d’images ou un chemin relatif (à `attribute::RootPath`) ou un chemin absolu vers un fichier image accessible par le serveur d’images.

## Restrictions {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Les sources d’images étrangères ne sont pas couvertes par le mécanisme d’image par défaut ; une erreur est renvoyée si une source d’image étrangère n’est pas valide.

## Par défaut {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Hérité de `default::DefaultImage` si elle n’est pas définie. S’il est défini mais vide, le comportement de l’image par défaut est désactivé, même si `default::DefaultImage` est défini.

## Voir aussi {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
