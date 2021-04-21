---
description: Horodatage de la modification. Indique la date et l’heure de la dernière modification de cette vignette.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Horodatage de la modification. Indique la date et l’heure de la dernière modification de cette vignette.

Si `attribute::UseLastModified` est défini, les valeurs les plus récentes `vignette::TimeStamp` et `catalog::TimeStamp`de la vignette et de tous les matériaux impliqués dans la requête sont renvoyées dans la réponse HTTP en tant qu&#39;en-tête modifié en dernier.

>[!NOTE]
>
>L’heure réelle du fichier de vignettes n’est jamais utilisée à cette fin.

`catalog::TimeStamp` est également utilisée pour la validation du cache basée sur un catalogue (voir  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Propriétés {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valeur Date/Heure au format Java. Il peut s’agir du nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*: *[!DNL ss]*GMT  *[!DNL offset]*

* *[!DNL hh]* est compris entre 0 et 23.
* *[!DNL zzz]* est un code de fuseau horaire de 3 ou 4 caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, &quot;PST&quot; pour l’heure du Pacifique, par rapport à &quot;PDT&quot; pour l’heure d’été du Pacifique).
* *[!DNL offset]* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, &#39;PDT&#39; est équivalent à &#39;GMT -7&#39;.

Tous les éléments des valeurs de date et heure formatées de chaîne doivent être présents. Si la valeur date/heure n&#39;est pas correctement formatée, elle est ignorée et l&#39;heure de modification du fichier [ ! DNL *[!DNL catalog]*.ini] sera utilisée à la place.

## Par défaut {#section-562c221d2e8b4a97ab5e9a3605f22140}

`attribute::TimeStamp` est le champ est vide ou absent.

## Voir aussi {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribut ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319),  [attribut::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
