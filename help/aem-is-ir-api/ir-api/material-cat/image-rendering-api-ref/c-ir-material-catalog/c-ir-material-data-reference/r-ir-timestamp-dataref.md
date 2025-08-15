---
title: Horodatage
description: Horodatage de modification du fichier. Spécifie la date et l’heure de la dernière modification des fichiers d’image et/ou de données joints à cet enregistrement de catalogue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---

# Horodatage{#timestamp}

Horodatage de modification du fichier. Spécifie la date et l’heure de la dernière modification des fichiers d’image et/ou de données joints à cet enregistrement de catalogue.

Si `attribute::UseLastModified` est défini, la plus récente des valeurs et `catalog::TimeStamp` `vignette::TimeStamp` de tous les matériaux et de la vignette impliquée dans la demande est renvoyée dans la réponse HTTP en tant qu’en-tête de dernière modification.

>[!NOTE]
>
>Les heures réelles des fichiers d’image ou de données joints à cette notice de catalogue ne sont jamais utilisées à cette fin.

Le `catalog::TimeStamp` est également utilisé pour la validation du cache basé sur le catalogue (voir [attribute ::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Propriétés {#section-42f09e375e72492b87a3a486da7df808}

Valeur de date et heure au format Java™. Il peut s’agir soit du nombre entier de millisecondes depuis minuit, le 1er janvier 1970 UTC/GMT, soit d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* se trouve dans la plage 0 à 23.
* *[!DNL zzz]* est un code de fuseau horaire à trois ou quatre caractères, tel que « GMT » ou « PST ». L’heure d’été doit être prise en compte dans le code de fuseau horaire. Par exemple, « PST » pour l’heure normale du Pacifique, contre « PDT » pour l’heure avancée du Pacifique.
* *[!DNL offset]* correspond au décalage de fuseau horaire en heures ou:minutes heures par rapport à GMT. Par exemple, &#39;PDT&#39; équivaut à &#39;GMT -7&#39;.

Tous les éléments de valeurs de date/heure au format chaîne doivent être présents. Si la valeur de date/heure n’est pas formatée correctement, elle est ignorée et l’heure de modification du *fichier .ini catalogue* est utilisée à la place.

## Par défaut {#section-e2c126c9e7294662b23944ab8d14866b}

Le `attribute::TimeStamp` champ est vide ou absent.

## Voir aussi {#section-876f1d1b50dc4501b605820015a29451}

[attribute ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute ::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute ::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
