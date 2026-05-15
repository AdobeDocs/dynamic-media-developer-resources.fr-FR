---
title: TimeStamp
description: Si « attribute::UseLastModified » est défini, la valeur « catalog::TimeStamp » est renvoyée dans la réponse HTTP en tant qu’en-tête HTTP Last-Modified.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
TQID: 'https://experienceleague.adobe.com/Am7JECwqMWbky2JrHKqZV1BJ7ef06JP9Sy-g9uUo8tw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 1%

---

# TimeStamp{#timestamp}

Si `attribute::UseLastModified` est défini, la valeur `catalog::TimeStamp` est renvoyée dans la réponse HTTP sous la forme d’un en-tête HTTP Last-Modified . L’en-tête Last-Modified est toujours renvoyé pour les contenus statiques, même si `attribute::UseLastModified` n’est pas défini.

Pour les contenus d’image et de SVG, `catalog::TimeStamp` est également utilisé pour la validation du cache catalogue (voir [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Propriétés {#section-2298a384b5cb43929542655c5a49beb2}

Valeur de date/heure au format Java. Peut être le nombre entier de millisecondes écoulées depuis minuit, 1er janvier 1970 UTC/GMT, ou une valeur de chaîne date/heure avec l’un des formats suivants :

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`* : *`mm`* : *`ss`* GMT *`offset`*

*`hh`* est compris entre 0 et 23.

*`zzz`* code de fuseau horaire à trois ou quatre caractères tel que &#39;GMT&#39; ou &#39;PST&#39;. Compte de l’heure d’été dans le code de fuseau horaire. Par exemple, « PST » pour l’heure standard du Pacifique, contre « PDT » pour l’heure d’été du Pacifique).

*`offset`* est un décalage horaire, en heures ou en `hours:minutes`, par rapport à GMT. Par exemple, « PDT » équivaut à « GMT -7 ».

Tous les éléments des valeurs de date et d’heure au format chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier `*`catalog`*.ini` est utilisée à la place.

## Par défaut {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` si le champ est vide ou absent.

## Voir aussi {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
