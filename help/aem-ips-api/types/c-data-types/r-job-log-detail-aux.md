---
description: Contient des messages supplémentaires associés au message principal du journal des tâches (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.
seo-description: Contient des messages supplémentaires associés au message principal du journal des tâches (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Scene7 Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

Contient des messages supplémentaires associés au message principal du journal des tâches (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | Message auxiliaire. |
| ` *`logType`*` | `xsd:string` | Type de journal : `IPSJobLog.gcUploadWarning` ou `IPSJobLog.gcUploadError`. |
| ` *`dateCreated`*` | `xsd:dateTime` | Date de création du journal des tâches auxiliaire. |

