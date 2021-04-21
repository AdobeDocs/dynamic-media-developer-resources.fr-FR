---
description: Horodatage de modification d’image par défaut. Fournit une valeur par défaut pour catalog TimeStamp.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 2%

---


# TimeStamp{#timestamp}

Horodatage de modification d’image par défaut. Fournit une valeur par défaut pour catalog::TimeStamp.

Si ce n&#39;est pas spécifié, le serveur utilisera la date et l&#39;heure de modification de ce fichier [!DNL *`catalog`*.ini].

## Propriétés {#section-647066e62ce44a84b627fdd0b2f7cfec}

Date/heure. Il peut s’agir du nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* est compris entre 0 et 23.

*`zzz`* est un code de fuseau horaire de 3 ou 4 caractères tel que  `GMT` ou  `PST`. L&#39;heure d&#39;été doit être prise en compte dans le code de fuseau horaire (p. ex. `PST` pour l&#39;heure d&#39;été du Pacifique, par rapport à `PDT` pour l&#39;heure d&#39;été du Pacifique).

*`offset`* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, `PDT` est équivalent à `GMT -7`.

Tous les éléments des valeurs de date et heure formatées de chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier [!DNL *`catalog`*.ini] est utilisée à la place.

## Par défaut {#section-ac465313c97943ed97d41ea852329177}

S’il est vide ou non défini, le serveur utilise l’heure de modification du fichier `*`catalog`*.ini`.

## Voir aussi {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalogue ::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [attribut::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [attribut::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
