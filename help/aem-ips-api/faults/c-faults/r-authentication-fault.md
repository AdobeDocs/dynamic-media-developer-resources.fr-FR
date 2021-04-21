---
description: Lancé lorsqu’un utilisateur ne peut pas être authentifié.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 18%

---


# authenticationFault{#authenticationfault}

Lancé lorsqu’un utilisateur ne peut pas être authentifié.

Syntaxe

## Types de défaillance {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Défaillance |
|---|---|
| 1 0000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Champs par défaut {#section-1fe84846a7154b03ab49552810ee9ac3}

| Nom | Type | Description |
|---|---|---|
| `code` | `xsd:int` | ID de panne |
| `reason` | `xsd:string` | Un message informatif décrivant la faute. |
