---
title: Horodatage
description: Si 'attribute ::UseLastModified' est défini, la valeur 'catalog ::TimeStamp' est renvoyée dans la réponse HTTP en tant qu’en-tête HTTP Last-Modified.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---

# Horodatage{#timestamp}

Si `attribute::UseLastModified` est défini, la `catalog::TimeStamp` valeur est renvoyée dans la réponse HTTP sous forme d’en-tête HTTP Last-Modified. L’en-tête Last-Modified est toujours renvoyé pour le contenu statique, même s’il `attribute::UseLastModified` n’est pas défini.

Pour les contenus image et SVG, `catalog::TimeStamp` est également utilisé pour la validation du cache basée sur le catalogue (voir [attribute ::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Propriétés {#section-2298a384b5cb43929542655c5a49beb2}

Valeur de date et heure au format Java. Il peut s’agir soit du nombre entier de millisecondes depuis minuit, le 1er janvier 1970 UTC/GMT, soit d’une valeur de chaîne date/heure avec l’un des formats suivants :

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* se trouve dans la plage 0 - 23.

*`zzz`* est un code de fuseau horaire à trois ou quatre caractères, tel que « GMT » ou « PST ». Tenez compte de l’heure d’été dans le code de fuseau horaire. Par exemple, « PST » pour l’heure normale du Pacifique, contre « PDT » pour l’heure avancée du Pacifique).

*`offset`* correspond au décalage de fuseau horaire en heures ou `hours:minutes`, par rapport à GMT. Par exemple, &#39;PDT&#39; équivaut à &#39;GMT -7&#39;.

Tous les éléments de valeurs de date/heure formatées par chaîne doivent être présents. Si la valeur de date/heure n’est pas formatée correctement, elle est ignorée et l’heure de modification du `*`fichier catalogue`*.ini` est utilisée à la place.

## Par défaut {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` si le champ est vide ou absent.

## Voir aussi {#section-c42a427aa4794c548408dc4de028d578}

[attribute ::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute ::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute ::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
