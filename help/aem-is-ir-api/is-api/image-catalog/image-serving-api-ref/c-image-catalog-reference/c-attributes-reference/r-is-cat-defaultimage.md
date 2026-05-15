---
description: Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser au cas où un fichier image serait introuvable et où defaultImage= n’est pas spécifié dans la requête.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
TQID: 'https://experienceleague.adobe.com/UcxsxmZBxozuJJh6FdBk-y166UZucXkbPbgfrS5ezEg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 1%

---

# DefaultImage{#defaultimage}

Image de réponse par défaut. Indique l’image ou l’entrée de catalogue à utiliser au cas où un fichier image serait introuvable et où defaultImage= n’est pas spécifié dans la requête.

Il peut s’agir d’une entrée de catalogue (y compris un modèle) ou d’un chemin d’accès relatif (à `attribute::RootPath`) ou absolu au fichier image. Utile pour remplacer des images manquantes par des images par défaut.

## Propriétés {#section-b6d8193827c34e5f948792aba8b8daaf}

Chaîne de texte. Si spécifié, doit être une valeur de `catalog::Id` valide dans ce catalogue d’images ou un chemin relatif (vers `attribute::RootPath`) ou absolu vers un fichier image accessible par le serveur d’images.

## Restrictions {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Les sources d’images étrangères ne sont pas couvertes par le mécanisme d’image par défaut. Une erreur est renvoyée si une source d’images étrangères n’est pas valide.

## Par défaut {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Hérité de `default::DefaultImage` si non défini. Si défini mais vide, le comportement d’image par défaut est désactivé, même si `default::DefaultImage` est défini.

## Voir aussi {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
