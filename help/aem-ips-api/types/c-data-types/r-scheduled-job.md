---
description: Tâche planifiée pour être exécutée.
seo-description: Tâche planifiée pour être exécutée.
seo-title: ScheduledJob
solution: Experience Manager
title: ScheduledJob
topic: Scene7 Image Production System API
uuid: cf0db523-2138-48c6-abbd-460a961e7de1
translation-type: tm+mt
source-git-commit: 26fb6212c3106deb7b088020d9f2993e40dec20b

---


# ScheduledJob{#scheduledjob}

Tâche planifiée pour être exécutée.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` |  poignée. |
| ` *`jobHandle`*` | `xsd:string` | Poignée de tâche planifiée. |
| ` *`nom`*` | `xsd:string` | Nom de la tâche. |
| ` *`originalName`*` | `xsd:string` | Nom d’origine de la tâche planifiée. |
| ` *`type`*` | `xsd:string` | Type de tâche. |
| ` *`submitUserEmail`*` | `xsd:string` | Adresse électronique de l’utilisateur qui a planifié la tâche. |
| ` *`locale`*` | `xsd:string` | Paramètres régionaux à utiliser pour les détails du journal des tâches et les  par courrier électronique. Les paramètres régionaux sont spécifiés comme `<language_code>[- <country_code>]`, où le code de langue est un code à deux lettres en minuscules, comme spécifié par ISO-639, et le code de pays facultatif est un code à deux lettres en majuscules, comme spécifié par ISO-3166. Par exemple, la chaîne de paramètres régionaux pour l’anglais (Etats-Unis) serait : `en-US`. |
| ` *`description`*` | `xsd:string` | Description de la tâche telle qu’elle a été initialement spécifiée dans `submitJob`. |
| ` *`execSchedule`*` | `xsd:string` | Lorsque l’exécution de la tâche est planifiée. |
| ` *`nextFireTime`*` | `xsd:dateTime` | Date, heure et fuseau horaire du déclenchement de la tâche. |
| ` *`timeZone`*` | `xsd:dateTime` | Fuseau horaire de la tâche planifiée. |
| ` *`triggerState`*` | `xsd:int` | Choix de l’état de déclenchement de tâche. |
| ` *`imageServingPublishJob`*` | `types:ImageServingPublishJob` | Détails de la tâche pour une tâche de publication de diffusion d’images. |
| ` *`imageServingRenderJob`*` | `types:ImageServingRenderJob` | Détails de la tâche pour une tâche de rendu d’image. |
| ` *`videoPublishJob`*` | `types:VideoPublishJob` | Détails de la tâche pour une tâche de publication vidéo. Voir [VideoPublishJob](https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_scheduled_job.html). |
| ` *`serverDirectoryPublishJob`*` | `types:ServerDirectoryPublishJob` | Détails de la tâche pour une tâche de publication dans le répertoire du serveur. |
| ` *`uploadDirectoryJob`*` | `types:UploadDirectoryJob` | Détails de la tâche pour une tâche de répertoire de téléchargement. |
| ` *`uploadUrlsJob`*` | `types:UploadUrlsJob` | Détails de la tâche pour une tâche d’URL de téléchargement. |
| ` *`optimizeImagesJob`*` | `types:OptimizeImagesJob` |  |
| ` *`ripPdfsJob`*` | `types:RipPdfsJob` |  |
| ` *`reprocessAssetsJob`*` | `types:ReprocessAssetsJob` |  |
| ` *`exportJob`*` | `types:ExportJob` | Autoriser l’exportation autorisée de fichiers précédemment téléchargés. Voir Tâche [d’exportation](https://marketing.adobe.com/resources/help/en_US/s7/ips_api/types/r_scheduled_job.html). |

## Remarques {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Lorsque vous spécifiez une valeur de type de tâche dans `submitJob`, le système renvoie une tâche en fonction de ce type. Les tâches suivantes peuvent être renvoyées :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`

