---
title: TimeStamp
description: Horodatage de modification du fichier. Indique la date/l’heure de la dernière modification des fichiers image et/ou données associés à cet enregistrement de catalogue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 1%

---

# TimeStamp{#timestamp}

Horodatage de modification du fichier. Indique la date/l’heure de la dernière modification des fichiers image et/ou données associés à cet enregistrement de catalogue.

Si `attribute::UseLastModified` est défini, les valeurs `catalog::TimeStamp` et `vignette::TimeStamp` les plus récentes de tous les matériaux et la vignette impliquée dans la requête sont renvoyées dans la réponse HTTP en tant qu’en-tête modifié en dernier.

>[!NOTE]
>
>Les heures réelles des fichiers d’image ou de données associés à cet enregistrement de catalogue ne sont jamais utilisées à cette fin.

`catalog::TimeStamp` est également utilisé pour la validation du cache basée sur le catalogue (voir [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Propriétés {#section-42f09e375e72492b87a3a486da7df808}

Valeur de date/heure au format Java™. Il peut s’agir du nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]* : *[!DNL mm]* : *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]* : *[!DNL mm]* : *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* est compris entre 0 et 23.
* *[!DNL zzz]* est un code de fuseau horaire de trois ou quatre caractères tel que &quot;GMT&quot; ou &quot;PST&quot;. L’heure d’été doit être prise en compte dans le code de fuseau horaire. Par exemple, &quot;PST&quot; pour l’heure normale du Pacifique, et &quot;PDT&quot; pour l’heure d’été du Pacifique.
* *[!DNL offset]* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, &quot;PDT&quot; équivaut à &quot;GMT -7&quot;.

Tous les éléments de valeurs date/heure au format chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier *catalog*.ini est utilisée à la place.

## Par défaut {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` est le champ vide ou non présent.

## Voir aussi {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
