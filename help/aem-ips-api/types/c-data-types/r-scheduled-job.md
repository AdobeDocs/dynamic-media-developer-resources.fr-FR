---
description: Tâche planifiée.
solution: Experience Manager
title: ScheduledJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 4%

---

# ScheduledJob{#scheduledjob}

Tâche planifiée.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Poignée de la société. |
| `*`jobHandle`*` | `xsd:string` | Gestionnaire de tâches planifiées. |
| `*`name`*` | `xsd:string` | Nom de la tâche. |
| `*`originalName`*` | `xsd:string` | Nom original de la tâche planifiée. |
| `*`type`*` | `xsd:string` | Type de tâche. |
| `*`submitUserEmail`*` | `xsd:string` | Adresse électronique de l’utilisateur qui a planifié la tâche. |
| `*`locale`*` | `xsd:string` | Paramètre régional à utiliser pour les détails du journal des tâches et la localisation des emails. Les paramètres régionaux sont spécifiés comme suit : `<language_code>[- <country_code>]`, où le code de langue est un code à deux lettres en minuscules, comme spécifié par la norme ISO-639, et le code de pays facultatif est un code à deux lettres en majuscules, comme spécifié par la norme ISO-3166. Par exemple, la chaîne du paramètre régional pour l’anglais (États-Unis) serait : `en-US`. |
| `*`description`*` | `xsd:string` | Description de la tâche telle qu’elle est spécifiée à l’origine dans `submitJob`. |
| `*`execSchedule`*` | `xsd:string` | Lorsque l’exécution de la tâche est planifiée. |
| `*`nextFireTime`*` | `xsd:dateTime` | Date, heure et fuseau horaire du déclenchement de la tâche. |
| `*`timeZone`*` | `xsd:dateTime` | Fuseau horaire de la tâche planifiée. |
| `*`triggerState`*` | `xsd:int` | Choix de l’état de déclenchement de la tâche. |
| `*`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Détails de la tâche pour une tâche de publication de diffusion d’image. |
| `*`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Détails de la tâche pour une tâche de rendu d’image. |
| `*`videoPublishJob`*` | `types:VideoPublishJob` | Détails de la tâche pour une tâche de publication vidéo. Voir [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |
| `*`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Détails de la tâche pour une tâche de publication dans un répertoire de serveur. |
| `*`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Détails de la tâche pour une tâche de téléchargement de répertoire. |
| `*`uploadUrlsJob`*` | `types:UploadUrlsJob` | Détails de la tâche pour une tâche de téléchargement d’URL. |
| `*`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| `*`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| `*`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| `*`exportJob`*` | `types:ExportJob` | Autoriser l’exportation autorisée des fichiers précédemment chargés. Voir [Tâche d’exportation](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html). |

## Remarques {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Lorsque vous spécifiez une valeur de type de tâche dans `submitJob`, le système renvoie une tâche en fonction de ce type. Les tâches suivantes peuvent être renvoyées :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
