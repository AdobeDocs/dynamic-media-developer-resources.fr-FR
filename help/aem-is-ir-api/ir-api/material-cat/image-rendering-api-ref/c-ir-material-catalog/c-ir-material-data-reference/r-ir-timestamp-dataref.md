---
description: Horodatage de modification du fichier. Indique la date et l’heure de la dernière modification des fichiers d’image et/ou de données joints à cet enregistrement de catalogue.
seo-description: Horodatage de modification du fichier. Indique la date et l’heure de la dernière modification des fichiers d’image et/ou de données joints à cet enregistrement de catalogue.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Scene7 Image Serving - Image Rendering API
uuid: 77ce8bee-7b55-4ff8-8dfb-ebd3ce9c7a8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TimeStamp{#timestamp}

Horodatage de modification du fichier. Indique la date et l’heure de la dernière modification des fichiers d’image et/ou de données joints à cet enregistrement de catalogue.

Si `attribute::UseLastModified` est défini, les valeurs les plus récentes de tous les matériaux `catalog::TimeStamp` et `vignette::TimeStamp` de la vignette impliquée dans la requête sont renvoyées dans la réponse HTTP sous la forme d’un en-tête modifié en dernier.

>[!NOTE] {class=&quot;- rubrique/note &quot;}
>
>Les heures réelles des fichiers d’image ou de données joints à cet enregistrement de catalogue ne sont jamais utilisées à cette fin.

`catalog::TimeStamp` est également utilisée pour la validation du cache basée sur un catalogue (voir ` [attribute::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4)`).

## Propriétés {#section-42f09e375e72492b87a3a486da7df808}

Valeur Date/Heure au format Java. Il peut s’agir du nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* GMT *[!DNL offset]*

* *[!DNL hh]* se trouve dans la plage 0 à 23.
* *[!DNL zzz]* est un code de fuseau horaire de 3 ou 4 caractères, tel que &quot;GMT&quot; ou &quot;PST&quot;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, &quot;PST&quot; pour l’heure d’été du Pacifique, par rapport à &quot;PDT&quot; pour l’heure d’été du Pacifique).
* *[!DNL offset]* est un décalage de fuseau horaire en heures ou heures:minutes, par rapport à GMT. Par exemple, &quot;PDT&quot; est équivalent à &quot;GMT -7&quot;.

Tous les éléments des valeurs de date/heure formatées de chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier *catalog*.ini est utilisée à la place.

## Par défaut {#section-e2c126c9e7294662b23944ab8d14866b}

`attribute::TimeStamp` est le champ est vide ou inexistant.

## Voir aussi {#section-876f1d1b50dc4501b605820015a29451}

[attribut::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [attribut::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d), [attribut::CacheValidationPolicy](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md#reference-2d71679733474d8aa116db6ceba87fa4), [vignette::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
