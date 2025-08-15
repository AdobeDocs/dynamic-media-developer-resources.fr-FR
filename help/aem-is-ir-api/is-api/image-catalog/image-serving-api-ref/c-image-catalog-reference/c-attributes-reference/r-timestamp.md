---
title: TimeStamp
description: Date et heure de modification de l’image par défaut. Elle fournit une valeur par défaut pour le catalogue TimeStamp.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Date et heure de modification de l’image par défaut. Fournit une valeur par défaut pour catalog::TimeStamp.

S’il n’est pas spécifié, le serveur utilise la date/l’heure de modification de ce fichier [!DNL *`catalog`*.ini].

## Propriétés {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valeur de date/heure. Il peut s’agir d’un nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

La valeur date/heure *`mm`*/ *`dd`*/ *`yyyy`* *`hh`* : *`mm`* : *`ss zzz`*

La valeur date/heure *`mm`*/ *`dd`*/ *`yyyy`* *`hh`* : *`mm`* : *`ss`* GMT *`offset`*

La valeur temporelle *`hh`* est comprise entre 0 et 23.

Le *`zzz`* de valeur temporelle est un code de fuseau horaire à trois ou quatre caractères, tel que `GMT` ou `PST`. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, `PST` pour l’heure standard du Pacifique, contre `PDT` pour l’heure d’été du Pacifique).

La valeur temporelle *`offset`* est un décalage horaire, exprimé en heures ou en heures:minutes par rapport à GMT. Par exemple, `PDT` équivaut à `GMT -7`.

Tous les éléments des valeurs de date et d’heure au format chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier [!DNL *`catalog`*.ini] est utilisée à la place.

## Par défaut {#section-ac465313c97943ed97d41ea852329177}

Si vide ou non défini, le serveur utilise l’heure de modification de ce fichier `*`catalogue`*.ini`.

## Voir aussi {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
