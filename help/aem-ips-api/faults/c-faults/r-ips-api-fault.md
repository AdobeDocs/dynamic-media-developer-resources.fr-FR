---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 48be47f6-4c1c-4f19-afa7-f643e504c287
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '25'
ht-degree: 36%

---

# ipsApiFault{#ipsapifault}

Syntaxe

## Types de défaillance {#section-425697675cac4b2ab5c48bd463956401}

| ID | Par défaut |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## Champs par défaut {#section-37fe1aef1d5f4ca480071ca933aba826}

| Nom | Type | Description |
|---|---|---|
| `code` | `xsd:int` | Identifiant de défaillance |
| `reason` | `xsd:string` | Un message informatif décrivant l’erreur. |
