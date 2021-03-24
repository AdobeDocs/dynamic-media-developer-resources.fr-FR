---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 28%

---


# ipsApiFault{#ipsapifault}

Syntaxe

## Types de défaillance {#section-425697675cac4b2ab5c48bd463956401}

| ID | Défaillance |
|---|---|
| 3 0000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## Champs par défaut {#section-37fe1aef1d5f4ca480071ca933aba826}

| Nom | Type | Description |
|---|---|---|
| `code` | `xsd:int` | ID de panne |
| `reason` | `xsd:string` | Un message informatif décrivant la faute. |

