---
description: Informations du journal des tâches.
seo-description: Informations du journal des tâches.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Dynamic Media Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '65'
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

