---
description: Informations du journal des tâches.
seo-description: Informations du journal des tâches.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Scene7 Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JobLogDetail{#joblogdetail}

Informations du journal des tâches.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | Messages dans le journal des tâches. |
| ` *`logType`*` | `xsd:string` | Type de fichier journal des tâches. |
| ` *`assetName`*` | `xsd:string` | Nom du fichier dans le journal des tâches (facultatif). |
| ` *`assetType`*` | `xsd:string` | Choix du type de fichier. |
| ` *`assetHandle`*` | `xsd:string` | Identifiant de ressource référencé dans le journal des tâches. |
| ` *`auxArray`*` | `types:JobLogDetailAuxArray` | Fournit des informations supplémentaires détaillées sur le journal des tâches au-delà des cinq types décrits ci-dessus. |

