---
description: Tâche planifiée pour s’exécuter.
solution: Experience Manager
title: Tâche planifiée
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c0084d10-ce38-4a01-9246-aaec44abc8eb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 4%

---

# [!DNL ScheduledJob]{#scheduledjob}

Tâche planifiée pour s’exécuter.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| companyHandle | `xsd:string` | Identifiant de la société. |
| jobHandle | `xsd:string` | Traitement des tâches planifiées. |
| nom | `xsd:string` | Nom du traitement. |
| originalName | `xsd:string` | Nom d’origine de la tâche planifiée. |
| type | `xsd:string` | Type de traitement. |
| submitUserEmail | `xsd:string` | Adresse e-mail de l’utilisateur qui a planifié la tâche. |
| local | `xsd:string` | Paramètres régionaux à utiliser pour les détails du journal de tâches et la localisation des e-mails. Les paramètres régionaux sont spécifiés sous la forme `<language_code>[- <country_code>]`, où le code de langue est un code à deux lettres en minuscules spécifié par la norme ISO-639, et le code de pays facultatif est un code à deux lettres en majuscules spécifié par la norme ISO-3166. Par exemple, la chaîne des paramètres régionaux pour l’anglais (États-Unis) serait : `en-US`. |
| description | `xsd:string` | Description du traitement telle qu’initialement spécifiée dans `submitJob`. |
| execSchedule | `xsd:string` | Lorsque l’exécution du traitement est planifiée. |
| nextFireTime | `xsd:dateTime` | Date, heure et fuseau horaire du déclenchement de la tâche. |
| timeZone | `xsd:dateTime` | Fuseau horaire de la tâche planifiée. |
| triggerState | `xsd:int` | Choix de l’état de déclenchement de la tâche. |
| imageServingPublishJob | `types:ImageServingPublishJob` | Détails de la tâche pour une image diffusant la tâche de publication. |
| imageServingRenderJob | `types:ImageServingRenderJob` | Détails d’une tâche de rendu d’image. |
| videoPublishJob | `types:VideoPublishJob` | Détails de la tâche pour une tâche de publication vidéo. Voir [VideoPublishJob](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=fr). |
| serverDirectoryPublishJob | `types:ServerDirectoryPublishJob` | Détails d’un traitement de publication dans l’annuaire du serveur. |
| uploadDirectoryJob | `types:UploadDirectoryJob` | Détails d’une tâche de répertoire de chargement. |
| uploadUrlsJob | `types:UploadUrlsJob` | Détails d’une tâche de chargement d’URL. |
| optimizerImagesJob | `types:OptimizeImagesJob` | |
| ripPdfsJob | `types:RipPdfsJob` | |
| reprocessAssetsJob | `types:ReprocessAssetsJob` | |
| exportJob | `types:ExportJob` | Autoriser l&#39;export des fichiers précédemment chargés Voir [&#x200B; Tâche d’exportation &#x200B;](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-production-api/data-types/r-scheduled-job.html?lang=fr). |

## Remarques {#section-34ec157f281f412f9f0f6e861e6ed0cd}

Lorsque vous spécifiez une valeur de type de tâche dans `submitJob`, le système renvoie une tâche en fonction de ce type. Les traitements suivants peuvent être renvoyés :

* `imageServingPublishJob`
* `imageRenderingPublishJob`
* `videoPublishJob`
* `serverDirectoryPublishJob`
* `uploadDirectorhJob`
* `uploadUrlsJob`
