---
description: Contient des messages supplémentaires associés au message principal du journal des tâches (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

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

