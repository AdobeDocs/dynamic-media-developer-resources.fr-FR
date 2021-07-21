---
description: Informations sur le log de la tâche.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

---

# JobLogDetail{#joblogdetail}

Informations sur le log de la tâche.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Messages dans le journal de la tâche. |
| `*`logType`*` | `xsd:string` | Type de fichier journal des tâches. |
| `*`assetName`*` | `xsd:string` | Nom de la ressource dans le journal des tâches (facultatif). |
| `*`assetType`*` | `xsd:string` | Choix du type de ressource. |
| `*`assetHandle`*` | `xsd:string` | Gestionnaire de ressources référencé dans le journal des tâches. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Fournit des informations supplémentaires détaillées sur le journal des tâches au-delà des cinq types décrits ci-dessus. |
