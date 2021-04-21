---
description: Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser au cas où un fichier image serait introuvable et que defaultImage= n’est pas spécifié dans la demande.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 2%

---


# DefaultImage{#defaultimage}

Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser au cas où un fichier image serait introuvable et que defaultImage= n’est pas spécifié dans la demande.

Il peut s’agir d’une entrée de catalogue (y compris un modèle) ou d’un chemin d’accès relatif (à `attribute::RootPath`) ou absolu au fichier image. Utile pour remplacer les images manquantes par des images par défaut.

## Propriétés {#section-b6d8193827c34e5f948792aba8b8daaf}

Chaîne de texte. Si spécifié, doit être soit une valeur `catalog::Id` valide dans ce catalogue d’images, soit un chemin d’accès relatif (à `attribute::RootPath`) ou absolu à un fichier d’image accessible par le serveur d’images.

## Restrictions {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Les sources d’images étrangères ne sont pas couvertes par le mécanisme d’image par défaut ; une erreur est renvoyée si une source d’image étrangère n’est pas valide.

## Par défaut {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Hérité de `default::DefaultImage` si elle n&#39;est pas définie. Si défini mais vide, le comportement d’image par défaut est désactivé, même si `default::DefaultImage` est défini.

## Voir aussi {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribut ::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [attribut::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catalogue::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), attribut::ErrorImage, attribut ::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)[
