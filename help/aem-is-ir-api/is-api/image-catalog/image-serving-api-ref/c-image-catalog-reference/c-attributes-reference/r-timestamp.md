---
description: Horodatage de modification d’image par défaut. Fournit une valeur par défaut pour catalog TimeStamp.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 2%

---

# TimeStamp{#timestamp}

Horodatage de modification d’image par défaut. Fournit une valeur par défaut pour catalog::TimeStamp.

Si elle n’est pas spécifiée, le serveur utilise la date/l’heure de modification de ce fichier [!DNL *`catalog`*.ini].

## Propriétés {#section-647066e62ce44a84b627fdd0b2f7cfec}

Date/heure. Peut être soit le nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, soit une valeur de chaîne date/heure avec l’un des formats suivants :

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* se trouve dans la plage 0 à 23.

*`zzz`* est un code de fuseau horaire de 3 ou 4 caractères, tel que  `GMT` ou  `PST`. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par ex. `PST` pour l’heure normale du Pacifique, par rapport à `PDT` pour l’heure d’été du Pacifique).

*`offset`* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, `PDT` équivaut à `GMT -7`.

Tous les éléments de valeurs date/heure formatées sous forme de chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier [!DNL *`catalog`*.ini] est utilisée à la place.

## Par défaut {#section-ac465313c97943ed97d41ea852329177}

S’il est vide ou non défini, le serveur utilise l’heure de modification de ce fichier `*`catalog`*.ini`.

## Voir aussi {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalogue ::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [attribut::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribut::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
