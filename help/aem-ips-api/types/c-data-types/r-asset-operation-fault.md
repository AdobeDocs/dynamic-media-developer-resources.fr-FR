---
description: Contient des informations sur les conditions d’avertissement ou d’erreur générées au cours d’une opération d’actif par lot. Les champs de code et de motif correspondent aux champs de message d'erreur qui auraient été générés pour l'opération non par lot équivalente.
seo-description: Contient des informations sur les conditions d’avertissement ou d’erreur générées au cours d’une opération d’actif par lot. Les champs de code et de motif correspondent aux champs de message d'erreur qui auraient été générés pour l'opération non par lot équivalente.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Dynamic Media Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---


# AssetOperationFault{#assetoperationfault}

Contient des informations sur les conditions d’avertissement ou d’erreur générées au cours d’une opération d’actif par lot. Les champs de code et de motif correspondent aux champs de message d&#39;erreur qui auraient été générés pour l&#39;opération non par lot équivalente.

Syntaxe

## Paramètres {#section-c906f052f43e4785ba46d92b514b0923}

| Nom | Type | Description |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Handle de ressource pour l&#39;opération ayant échoué. |
| `*`code`*` | `xsd:int` | Code d&#39;erreur d&#39;opération. |
| `*`motif`*` | `xsd:string` | Description ou raison de la défaillance. |

