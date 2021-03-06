---
description: Horodatage de modification du fichier. Indique la date/l’heure de dernière modification de l’image et/ou des fichiers de données associés à cet enregistrement de catalogue.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Horodatage de modification du fichier. Indique la date/l’heure de dernière modification de l’image et/ou des fichiers de données associés à cet enregistrement de catalogue.

If `attribute::UseLastModified` est définie, la plus récente de la variable `catalog::TimeStamp` et `vignette::TimeStamp` les valeurs de tous les matériaux et la vignette impliquée dans la requête sont renvoyées dans la réponse HTTP en tant qu’en-tête modifié en dernier.

>[!NOTE]
>
>Les heures réelles des fichiers d’image ou de données associés à cet enregistrement de catalogue ne sont jamais utilisées à cette fin.

`catalog::TimeStamp` est également utilisé pour la validation du cache basée sur le catalogue (voir [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Propriétés {#section-42f09e375e72492b87a3a486da7df808}

Date/heure au format Java. Peut être soit le nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, soit une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* se trouve dans la plage 0 à 23.
* *[!DNL zzz]* est un code de fuseau horaire de 3 ou 4 caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, &quot;PST&quot; pour l’heure normale du Pacifique, et &quot;PDT&quot; pour l’heure d’été du Pacifique).
* *[!DNL offset]* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, &quot;PDT&quot; équivaut à &quot;GMT -7&quot;.

Tous les éléments de valeurs date/heure formatées sous forme de chaîne doivent être présents. Si la valeur de date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification de la variable *catalogue* Le fichier .ini est utilisé à la place.

## Par défaut {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` est que le champ est vide ou n’est pas présent.

## Voir aussi {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
