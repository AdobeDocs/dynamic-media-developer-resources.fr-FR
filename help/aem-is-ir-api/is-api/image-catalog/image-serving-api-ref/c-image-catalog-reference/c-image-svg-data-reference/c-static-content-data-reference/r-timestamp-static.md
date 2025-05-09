---
title: TimeStamp
description: Si &grave;attribute::UseLastModified&grave; est défini, la valeur &grave;catalog::TimeStamp&grave; est renvoyée dans la réponse HTTP en tant qu’en-tête HTTP Last-Modified. L’en-tête Last-Modified est toujours renvoyé pour le contenu statique, même si "attribute::UseLastModified" n’est pas défini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Si `attribute::UseLastModified` est défini, la valeur `catalog::TimeStamp` est renvoyée dans la réponse HTTP en tant qu’en-tête HTTP Last-Modified. L’en-tête Last-Modified est toujours renvoyé pour le contenu statique, même si `attribute::UseLastModified` n’est pas défini.

Pour les contenus d’image et de SVG, `catalog::TimeStamp` est également utilisé pour la validation du cache basée sur le catalogue (voir [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Propriétés {#section-2298a384b5cb43929542655c5a49beb2}

Date/heure au format Java. Il peut s’agir du nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`* : *`mm`* : *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`* : *`mm`* : *`ss`* GMT *`offset`*

*`hh`* est compris entre 0 et 23.

*`zzz`* est un code de fuseau horaire de trois ou quatre caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. Compte pour l’heure d’été dans le code de fuseau horaire. Par exemple, &quot;PST&quot; pour l’heure normale du Pacifique, et &quot;PDT&quot; pour l’heure d’été du Pacifique).

*`offset`* est un décalage de fuseau horaire en heures ou `hours:minutes`, par rapport à GMT. Par exemple, &quot;PDT&quot; équivaut à &quot;GMT -7&quot;.

Tous les éléments de valeurs date/heure formatées sous forme de chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier `*`catalog`*.ini` est utilisée à la place.

## Par défaut {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` si le champ est vide ou non présent.

## Voir aussi {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
