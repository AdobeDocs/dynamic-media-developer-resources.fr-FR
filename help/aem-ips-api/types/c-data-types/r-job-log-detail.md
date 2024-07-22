---
description: Informations sur le log de la tâche.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

Informations sur le log de la tâche.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| logMessage | `xsd:string` | Messages dans le journal de la tâche. |
| logType | `xsd:string` | Type de fichier journal de la tâche. |
| assetName | `xsd:string` | Nom de la ressource dans le journal des tâches (facultatif). |
| assetType | `xsd:string` | Choix du type de ressource. |
| assetHandle | `xsd:string` | Gestionnaire de ressources référencé dans le journal des tâches. |
| auxArray | `types:JobLogDetailAuxArray` | Fournit des informations supplémentaires détaillées sur le journal des tâches au-delà des cinq types décrits ci-dessus. |
