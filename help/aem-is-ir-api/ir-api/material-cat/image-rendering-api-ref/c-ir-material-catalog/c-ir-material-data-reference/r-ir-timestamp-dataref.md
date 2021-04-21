---
description: Horodatage de modification de fichier. Indique la date et l’heure de la dernière modification des fichiers d’image et/ou de données joints à cet enregistrement de catalogue.
solution: Experience Manager
title: TimeStamp
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# TimeStamp{#timestamp}

Horodatage de modification de fichier. Indique la date et l’heure de la dernière modification des fichiers d’image et/ou de données joints à cet enregistrement de catalogue.

Si `attribute::UseLastModified` est défini, les valeurs `catalog::TimeStamp` et `vignette::TimeStamp` les plus récentes de tous les matériaux et de la vignette impliquée dans la demande sont renvoyées dans la réponse HTTP en tant qu&#39;en-tête modifié en dernier.

>[!NOTE]
>
>Les heures réelles des fichiers d&#39;image ou de données joints à cet enregistrement catalogue ne sont jamais utilisées à cette fin.

`catalog::TimeStamp` est également utilisée pour la validation du cache basée sur un catalogue (voir  ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Propriétés {#section-42f09e375e72492b87a3a486da7df808}

Valeur Date/Heure au format Java. Il peut s’agir du nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/  *[!DNL dd]*/  *[!DNL yyyy]* *[!DNL hh]*:  *[!DNL mm]*:  *[!DNL ss]* GMT  *[!DNL offset]*

* *[!DNL hh]* est compris entre 0 et 23.
* *[!DNL zzz]* est un code de fuseau horaire de 3 ou 4 caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, &quot;PST&quot; pour l’heure du Pacifique, par rapport à &quot;PDT&quot; pour l’heure d’été du Pacifique).
* *[!DNL offset]* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, &#39;PDT&#39; est équivalent à &#39;GMT -7&#39;.

Tous les éléments des valeurs de date et heure formatées de chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier *catalog*.ini est utilisée à la place.

## Par défaut {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` est le champ est vide ou absent.

## Voir aussi {#section-876f1d1b50dc4501b605820015a29451}

[attribut ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) ,  [attribut::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d),  [attribut::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4),  [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
