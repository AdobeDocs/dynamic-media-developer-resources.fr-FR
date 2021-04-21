---
description: Contient des informations sur les conditions d’avertissement ou d’erreur générées au cours d’une opération d’actif par lot. Les champs de code et de motif correspondent aux champs de message d'erreur qui auraient été générés pour l'opération non par lot équivalente.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

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

