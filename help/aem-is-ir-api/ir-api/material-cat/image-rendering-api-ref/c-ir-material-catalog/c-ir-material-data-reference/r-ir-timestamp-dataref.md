---
title: TimeStamp
description: Horodatage de modification du fichier. Indique la date et l’heure de la dernière modification des fichiers image et/ou de données joints à cet enregistrement de catalogue.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ecc7617c-c390-4f82-905d-45b825d0176d
TQID: 'https://experienceleague.adobe.com/wC-1FowmCBdznH7ERWSYp-3Dx7bKC7fZPJXLnaWhFLU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 6%

---

# TimeStamp{#timestamp}

Horodatage de modification du fichier. Indique la date et l’heure de la dernière modification des fichiers image et/ou de données joints à cet enregistrement de catalogue.

Si `attribute::UseLastModified` est défini, la plus récente des valeurs `catalog::TimeStamp` et `vignette::TimeStamp` de tous les matériaux et de la vignette impliqués dans la requête est renvoyée dans la réponse HTTP comme en-tête de dernière modification.

>[!NOTE]
>
>Les durées réelles des fichiers d’image ou de données joints à cet enregistrement de catalogue ne sont jamais utilisées à cet effet.

Le `catalog::TimeStamp` est également utilisé pour la validation du cache par catalogue (voir [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md)).

## Propriétés {#section-42f09e375e72492b87a3a486da7df808}

Valeur de date/heure au format Java™. Il peut s’agir d’un nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]* : *[!DNL mm]* : *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* est compris entre 0 et 23.
* *[!DNL zzz]* code de fuseau horaire à trois ou quatre caractères tel que &#39;GMT&#39; ou &#39;PST&#39;. L’heure d’été doit être prise en compte dans le code de fuseau horaire. Par exemple, « PST » pour l’heure standard du Pacifique, contre « PDT » pour l’heure d’été du Pacifique.
* *[!DNL offset]* correspond à un décalage horaire, en heures ou en heures:minutes par rapport à GMT. Par exemple, « PDT » équivaut à « GMT -7 ».

Tous les éléments des valeurs de date et d’heure au format chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier *catalog*.ini est utilisée à la place.

## Par défaut {#section-e2c126c9e7294662b23944ab8d14866b}

Le `attribute::TimeStamp` est le champ vide ou non présent.

## Voir aussi {#section-876f1d1b50dc4501b605820015a29451}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)

