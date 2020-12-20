---
description: Lancé lorsqu’un utilisateur authentifié ne dispose pas des autorisations suffisantes pour accomplir une tâche.
seo-description: Lancé lorsqu’un utilisateur authentifié ne dispose pas des autorisations suffisantes pour accomplir une tâche.
seo-title: authorizedFault
solution: Experience Manager
title: authorizedFault
topic: Scene7 Image Production System API
uuid: 8b8df22a-aa76-4cbd-9c14-89969c5f9620
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 22%

---


# authorizedFault{#authorizationfault}

Lancé lorsqu’un utilisateur authentifié ne dispose pas des autorisations suffisantes pour accomplir une tâche.

Syntaxe

## Types de défaillance {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | Défaillance |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 2001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 2002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 2003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 2004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 2005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 2006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 2007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 2008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 2009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## Champs par défaut {#section-4e3e41f41fea402a9ae314bfd05f663e}

| Nom | Type | Description |
|---|---|---|
| `code` | `xsd:int` | ID de panne |
| `reason` | `xsd:string` | Un message informatif décrivant la faute. |

