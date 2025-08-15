---
description: Contient des messages supplémentaires associés au message principal du log de traitement (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource en cours de traitement.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

Contient des messages supplémentaires associés au message principal du log de traitement (JobDetail). Inclut des avertissements et d’autres détails associés à la ressource en cours de traitement.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| logMessage | `xsd:string` | Un message auxiliaire. |
| logType | `xsd:string` | Type de journal : `IPSJobLog.gcUploadWarning` ou `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | Date de création du log de traitement auxiliaire. |
