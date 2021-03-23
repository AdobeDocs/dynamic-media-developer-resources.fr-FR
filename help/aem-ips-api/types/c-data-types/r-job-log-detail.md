---
description: Informations du journal des tâches.
seo-description: Informations du journal des tâches.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

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

