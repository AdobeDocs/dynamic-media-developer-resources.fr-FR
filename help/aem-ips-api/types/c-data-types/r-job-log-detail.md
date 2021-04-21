---
description: Informations du journal des tâches.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---


# JobLogDetail{#joblogdetail}

Informations du journal des tâches.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Messages dans le journal des tâches. |
| `*`logType`*` | `xsd:string` | Type de fichier journal de la tâche. |
| `*`assetName`*` | `xsd:string` | Nom du fichier dans le journal des tâches (facultatif). |
| `*`assetType`*` | `xsd:string` | Choix du type de fichier. |
| `*`assetHandle`*` | `xsd:string` | Handle de ressource référencé dans le journal des tâches. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Fournit des informations supplémentaires détaillées sur le journal des tâches au-delà des cinq types décrits ci-dessus. |

