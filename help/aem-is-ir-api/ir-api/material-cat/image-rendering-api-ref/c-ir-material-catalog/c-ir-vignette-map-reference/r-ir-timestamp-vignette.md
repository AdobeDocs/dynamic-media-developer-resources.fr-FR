---
title: Horodatage
description: Horodatage de modification. Indique la date et l’heure de la dernière modification de cette vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 1%

---

# Horodatage{#timestamp}

Horodatage de modification. Indique la date et l’heure de la dernière modification de cette vignette.

Si `attribute::UseLastModified` est défini, la valeur la plus récente `vignette::TimeStamp` et `catalog::TimeStamp`la valeur de la vignette et de tous les matériaux impliqués dans la requête sont renvoyées dans la réponse HTTP en tant qu’en-tête de dernière modification.

>[!NOTE]
>
>L’heure réelle du fichier de vignette n’est jamais utilisée à cette fin.

Le `catalog::TimeStamp` est également utilisé pour la validation du cache basé sur un catalogue. Voir [attribute ::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Propriétés {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valeur de date et heure au format Java™. Il peut s’agir soit du nombre entier de millisecondes depuis minuit, le 1er janvier 1970 UTC/GMT, soit d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]*GMT *[!DNL offset]*

* *[!DNL hh]* se trouve dans la plage 0 à 23.
* *[!DNL zzz]* est un code de fuseau horaire à trois ou quatre caractères, tel que « GMT » ou « PST ». L’heure avancée doit être prise en compte dans le code de fuseau horaire (par exemple, « PST » pour l’heure normale du Pacifique, par opposition à « PDT » pour l’heure avancée du Pacifique).
* *[!DNL offset]* correspond au décalage de fuseau horaire en heures ou:minutes heures par rapport à GMT. Par exemple, &#39;PDT&#39; équivaut à &#39;GMT -7&#39;.

Tous les éléments de valeurs de date/heure au format chaîne doivent être présents. Si la valeur de date et d’heure n’est pas correctement formatée, elle est ignorée et l’heure de modification de la variable [ ! DNL *[!DNL catalog]*.ini] est utilisé à la place.

## Par défaut {#section-562c221d2e8b4a97ab5e9a3605f22140}

Le `attribute::TimeStamp` champ est vide ou absent.

## Voir aussi {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalogue ::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribut ::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
