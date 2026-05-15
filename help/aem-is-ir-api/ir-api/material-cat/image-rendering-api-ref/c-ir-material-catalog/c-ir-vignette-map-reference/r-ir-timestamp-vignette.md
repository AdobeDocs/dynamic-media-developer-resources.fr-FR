---
title: TimeStamp
description: Horodatage de modification. Spécifie la date/l'heure de la dernière modification de cette vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a163727-9ac6-43ca-9afd-169ac6306124
TQID: 'https://experienceleague.adobe.com/lVoM4P1NUj-ugSgiBM5l-9L9wtTuGiZCKDjTnEGQa1A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# TimeStamp{#timestamp}

Horodatage de modification. Spécifie la date/l&#39;heure de la dernière modification de cette vignette.

Si `attribute::UseLastModified` est défini, la `vignette::TimeStamp` et la `catalog::TimeStamp`valeur les plus récentes de la vignette et de tous les éléments impliqués dans la requête sont renvoyés dans la réponse HTTP sous la forme d’un en-tête de dernière modification.

>[!NOTE]
>
>L’heure réelle du fichier de vignette n’est jamais utilisée à cette fin.

Le `catalog::TimeStamp` est également utilisé pour la validation du cache catalogue. Voir [attribute::CacheValidationPolicy](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cachevalidationpolicy.md).

## Propriétés {#section-c4a42c64e44d49238ef2ec31ebd82ac1}

Valeur de date/heure au format Java™. Il peut s’agir d’un nombre entier de millisecondes écoulées depuis minuit, le 1er janvier 1970 UTC/GMT, ou d’une valeur de chaîne date/heure avec l’un des formats suivants :

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]*: *[!DNL mm]*: *[!DNL ss]* *[!DNL zzz]*

*[!DNL mm]*/ *[!DNL dd]*/ *[!DNL yyyy]* *[!DNL hh]* : *[!DNL mm]*: *[!DNL ss]*&#x200B;GMT *[!DNL offset]*

* *[!DNL hh]* est compris entre 0 et 23.
* *[!DNL zzz]* code de fuseau horaire à trois ou quatre caractères tel que &#39;GMT&#39; ou &#39;PST&#39;. L’heure d’été doit être prise en compte dans le code de fuseau horaire (par exemple, « PST » pour l’heure standard du Pacifique, contre « PDT » pour l’heure d’été du Pacifique).
* *[!DNL offset]* correspond à un décalage horaire, en heures ou en heures:minutes par rapport à GMT. Par exemple, « PDT » équivaut à « GMT -7 ».

Tous les éléments des valeurs de date et d’heure au format chaîne doivent être présents. Si la valeur date/heure n’est pas correctement formatée, elle est ignorée et l’heure de modification du fichier [!DNL *[!DNL catalog]*.ini] est utilisée à la place.

## Par défaut {#section-562c221d2e8b4a97ab5e9a3605f22140}

Le `attribute::TimeStamp` est le champ vide ou non présent.

## Voir aussi {#section-ffa82b202be04dd9b87cba3c61d1ee24}

[attribute::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-timestamp.md#reference-8373ad4ee03d4e4b9a8fc96cf42b3181) , [catalog::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319), [attribute::UseLastModified](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-uselastmodified.md#reference-d2ab628c9e004fedbd38324866dbca1d)
