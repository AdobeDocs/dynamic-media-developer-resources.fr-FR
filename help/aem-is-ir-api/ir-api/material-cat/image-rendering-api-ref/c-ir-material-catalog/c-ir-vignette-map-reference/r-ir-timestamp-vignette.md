---
description: Horodatage de modification. Indique la date et l’heure de la dernière modification de cette vignette.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Horodatage de modification. Indique la date et l’heure de la dernière modification de cette vignette.

If `attribute::UseLastModified` est défini, le plus récent `vignette::TimeStamp` et `catalog::TimeStamp`la valeur de la vignette et de tous les matériaux impliqués dans la requête sont renvoyés dans la réponse HTTP en tant qu’en-tête modifié en dernier.

>[!NOTE]
>
>L’heure réelle du fichier de vignette n’est jamais utilisée à cette fin.

`catalog::TimeStamp` est également utilisé pour la validation du cache basée sur le catalogue (voir [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Propriétés {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Date/heure au format Java. Peut être soit le nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, soit une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* se trouve dans la plage 0 à 23.
* *[!DNL zzz]* est un code de fuseau horaire de 3 ou 4 caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, &quot;PST&quot; pour l’heure normale du Pacifique, et &quot;PDT&quot; pour l’heure d’été du Pacifique).
* *[!DNL offset]* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, &quot;PDT&quot; équivaut à &quot;GMT -7&quot;.

Tous les éléments de valeurs date/heure formatées sous forme de chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification de [!DNL *[!DNL catalog]*.ini] est utilisé à la place.

## Par défaut {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` est que le champ est vide ou n’est pas présent.

## Voir aussi {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalogue ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
