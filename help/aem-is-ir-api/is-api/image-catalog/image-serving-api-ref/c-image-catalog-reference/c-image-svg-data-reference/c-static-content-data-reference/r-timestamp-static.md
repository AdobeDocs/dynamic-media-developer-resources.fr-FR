---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fd60e5db-9219-41a8-947f-0d497b39e727
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Si `attribute::UseLastModified` est défini, la valeur `catalog::TimeStamp` est renvoyée dans la réponse HTTP sous la forme d&#39;un en-tête HTTP Dernière modification. L’en-tête Dernière modification est toujours renvoyé pour le contenu statique, même si `attribute::UseLastModified` n’est pas défini.

Pour le contenu image et SVG, `catalog::TimeStamp` est également utilisé pour la validation du cache basée sur un catalogue (voir ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Propriétés {#section-2298a384b5cb43929542655c5a49beb2}

Valeur Date/Heure au format Java. Peut être soit le nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, soit une valeur de chaîne date/heure avec l’un des formats suivants :

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* est compris entre 0 et 23.

*`zzz`* est un code de fuseau horaire de trois ou quatre caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. Compte pour l’heure d’été dans le code de fuseau horaire. Par exemple, &quot;PST&quot; pour l’heure normale du Pacifique, par rapport à &quot;PDT&quot; pour l’heure avancée du Pacifique).

*`offset`* est un décalage de fuseau horaire en heures ou  `hours:minutes`, par rapport à GMT. Par exemple, &#39;PDT&#39; est équivalent à &#39;GMT -7&#39;.

Tous les éléments des valeurs de date/heure formatées de chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier `*`catalog`*.ini` est utilisée à la place.

## Par défaut {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` si le champ est vide ou absent.

## Voir aussi {#section-c42a427aa4794c548408dc4de028d578}

[attribut::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [attribut::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribut::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
