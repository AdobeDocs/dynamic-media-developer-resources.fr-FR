---
description: Horodatage de modification par défaut. Fournit une valeur par défaut pour catalog TimeStamp et la vignette TimeStamp. Si elle n’est pas spécifiée, le serveur utilisera la date et l’heure de modification de ce fichier catalog.ini.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Horodatage de modification par défaut. Fournit une valeur par défaut pour catalog::TimeStamp et vignette::TimeStamp. Si elle n’est pas spécifiée, le serveur utilisera la date et l’heure de modification de ce fichier catalog.ini.

## Propriétés {#section-910e2562b41c47b78ee6216deeabbbd5}

Valeur Date/Heure au format Java. Il peut s’agir du nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

*[!DNL hh]* est compris entre 0 et 23.

*[!DNL zzz]* est un code de fuseau horaire de 3 ou 4 caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, &quot;PST&quot; pour l’heure du Pacifique, par rapport à &quot;PDT&quot; pour l’heure d’été du Pacifique).

*[!DNL offset]* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, &#39;PDT&#39; est équivalent à &#39;GMT -7&#39;.

Tous les éléments des valeurs de date et heure formatées de chaîne doivent être présents. Si la valeur date/heure n&#39;est pas correctement formatée, elle est ignorée et l&#39;heure de modification du fichier [ ! DNL *[!DNL catalog]*.ini] sera utilisée à la place.

## Par défaut {#section-65fb29a9ea2044df8cb9fe295eb14872}

S&#39;il est vide ou non défini, le serveur utilisera l&#39;heure de modification du fichier de ce fichier [ ! DNL *[!DNL catalog]*.ini].

## Voir aussi {#section-764188f9b1734ad1a6270f5fecd28532}

[catalogue ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1),  [attribut::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attribut::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
