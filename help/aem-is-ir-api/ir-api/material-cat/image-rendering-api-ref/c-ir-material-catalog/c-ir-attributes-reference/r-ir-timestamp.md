---
title: Horodatage
description: Horodatage de modification par défaut. Fournit une valeur par défaut pour l’horodatage du catalogue et l’horodatage de la vignette. Si cette valeur n’est pas spécifiée, le serveur utilise la date et l’heure de modification de ce fichier catalog.ini.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b6d8fa6-0ad9-4f72-8d6d-1427e5d59df3
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 1%

---

# Horodatage{#timestamp}

Horodatage de modification par défaut. Fournit une valeur par défaut pour `catalog::TimeStamp` et `vignette::TimeStamp`. Si cette valeur n’est pas spécifiée, le serveur utilise la date et l’heure de modification de ce fichier catalog.ini.

## Propriétés {#section-910e2562b41c47b78ee6216deeabbbd5}

Valeur de date et heure au format Java™. Il peut s’agir soit du nombre entier de millisecondes depuis minuit, le 1er janvier 1970 UTC/GMT, soit d’une valeur de chaîne date/heure avec l’un des formats suivants :

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

* *[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

*[!DNL hh]* se trouve dans la plage de 0 à 23.

*[!DNL zzz]* est un code de fuseau horaire à trois ou quatre caractères, tel que « GMT » ou « PST ». L’heure avancée doit être prise en compte dans le code de fuseau horaire (par exemple, « PST » pour l’heure normale du Pacifique, par opposition à « PDT » pour l’heure avancée du Pacifique).

*[!DNL offset]* correspond au décalage de fuseau horaire en heures ou:minutes heures par rapport à GMT. Par exemple, &#39;PDT&#39; équivaut à &#39;GMT -7&#39;.

Tous les éléments de valeurs de date/heure au format chaîne doivent être présents. Si la valeur de date et d’heure n’est pas correctement formatée, elle est ignorée et l’heure de modification de la variable [!DNL *[!DNL catalog]*.ini] est utilisé à la place.

## Par défaut {#section-65fb29a9ea2044df8cb9fe295eb14872}

Si vide ou non défini, le serveur utilise le délai de modification du fichier de ce [!DNL *[!DNL catalog]*.ini].

## Voir aussi {#section-764188f9b1734ad1a6270f5fecd28532}

[catalog ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignette ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1), [attribute ::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute ::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)
