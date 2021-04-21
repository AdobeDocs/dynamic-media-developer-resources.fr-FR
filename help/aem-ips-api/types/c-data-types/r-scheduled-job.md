---
description: Tâche planifiée pour exécution.
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 4%

---


# ScheduledJob{#scheduledjob}

Tâche planifiée pour exécution.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Poignée de société. |
| `*`jobHandle`*` | `xsd:string` | Poignée de tâche planifiée. |
| `*`name`*` | `xsd:string` | Nom de la tâche. |
| `*`originalName`*` | `xsd:string` | Nom original de la tâche planifiée. |
| `*`type`*` | `xsd:string` | Type de tâche. |
| `*`submitUserEmail`*` | `xsd:string` | Adresse électronique de l’utilisateur qui a planifié la tâche. |
| `*`locale`*` | `xsd:string` | Paramètres régionaux à utiliser pour les détails du journal des tâches et la localisation de courriel. Les paramètres régionaux sont spécifiés sous la forme `<language_code>[- <country_code>]`, où le code de langue est un code à deux lettres en minuscules, comme spécifié par ISO-639, et le code de pays facultatif est un code à deux lettres en majuscules, comme spécifié par ISO-3166. Par exemple, la chaîne de paramètres régionaux pour l’anglais (Etats-Unis) serait : `en-US`. |
| `*`description`*` | `xsd:string` | Description de la tâche telle que spécifiée à l&#39;origine dans `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | Date à laquelle l’exécution de la tâche est planifiée. |
| `*`nextFireTime`*` | `xsd:dateTime` | Date, heure et fuseau horaire de déclenchement de la tâche. |
| `*`timeZone`*` | `xsd:dateTime` | Fuseau horaire de la tâche planifiée. |
| `*`triggerState`*` | `xsd:int` | Choix de l’état de déclenchement de la tâche. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Détails de la tâche pour une tâche de publication avec image. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Détails de la tâche pour une tâche de rendu d’image. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | Détails de la tâche pour une tâche de publication vidéo. Voir [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Détails de la tâche pour une tâche de publication dans l’annuaire de serveurs. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Détails de la tâche pour une tâche de répertoire de téléchargement. |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | Détails de la tâche pour une tâche de téléchargement d’URL. |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | Autoriser l’exportation autorisée de fichiers précédemment téléchargés. Voir [Tâche d’exportation](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Remarques {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Lorsque vous spécifiez une valeur de type de tâche dans `submitJob`, le système renvoie une tâche en fonction de ce type. Les tâches suivantes peuvent être renvoyées :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

