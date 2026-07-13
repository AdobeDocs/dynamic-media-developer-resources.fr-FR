---
title: TimeStamp
description: Horodatage de modification par défaut. Fournit une valeur par défaut pour les paramètres TimeStamp de catalogue et TimeStamp de vignette. S’il n’est pas spécifié, le serveur utilise la date/l’heure de modification de ce fichier catalog.ini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
TQID: 'https://experienceleague.adobe.com/p3g5NQf25sagtaAYjdd4Vd8J6kZBAoLM8tSY42NPuOI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 7%

---

# TimeStamp{#timestamp}

Horodatage de modification par défaut. Fournit une valeur par défaut pour `catalog::TimeStamp` et `vignette::TimeStamp`. S’il n’est pas spécifié, le serveur utilise la date/l’heure de modification de ce fichier catalog.ini.

## Propriétés {#section-910e2562b41c47b78ee6216deeabbbd5}

Valeur de date/heure au format Java™. Peut être le nombre entier de millisecondes écoulées depuis minuit, 1er janvier 1970 UTC/GMT, ou une valeur de chaîne date/heure avec l’un des formats suivants :

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]* : *[!DNL mm]* : *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* est compris entre 0 et 23.

*[!DNL zzz]* code de fuseau horaire à trois ou quatre caractères tel que &#39;GMT&#39; ou &#39;PST&#39;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, « PST » pour l’heure standard du Pacifique, contre « PDT » pour l’heure d’été du Pacifique).

*[!DNL offset]* correspond à un décalage horaire, en heures ou en heures:minutes par rapport à GMT. Par exemple, « PDT » équivaut à « GMT -7 ».

Tous les éléments des valeurs de date et d’heure au format chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier [!DNL *[!DNL catalog]*.ini] est utilisée à la place.

## Par défaut {#section-65fb29a9ea2044df8cb9fe295eb14872}

S&#39;il est vide ou non défini, le serveur utilise l&#39;heure de modification de ce fichier [!DNL *[!DNL catalog]*.ini].

## Voir aussi {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)

