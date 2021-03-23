---
description: Contient des messages supplémentaires associés au message principal du journal des tâches (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.
seo-description: Contient des messages supplémentaires associés au message principal du journal des tâches (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

Contient des messages supplémentaires associés au message principal du journal des tâches (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Message auxiliaire. |
| `*`logType`*` | `xsd:string` | Type de journal : `IPSJobLog.gcUploadWarning` ou `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Date de création du journal des tâches auxiliaire. |

