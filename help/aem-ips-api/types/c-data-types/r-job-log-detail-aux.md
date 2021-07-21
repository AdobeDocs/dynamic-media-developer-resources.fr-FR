---
description: Contient des messages supplémentaires associés au message principal du log de traitement (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 7%

---

# JobLogDetailAux{#joblogdetailaux}

Contient des messages supplémentaires associés au message principal du log de traitement (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource traitée actuellement.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Un message auxiliaire. |
| `*`logType`*` | `xsd:string` | Type de journal : `IPSJobLog.gcUploadWarning` ou `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Date de création du journal des tâches auxiliaire. |
