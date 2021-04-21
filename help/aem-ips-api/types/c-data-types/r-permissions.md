---
description: Gère les droits d’accès, de modification, de création ou de suppression de fichiers par groupe.
solution: Experience Manager
title: Autorisation
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---


# Autorisation{#permission}

Gère les droits d’accès, de modification, de création ou de suppression de fichiers par groupe.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Poignée de groupe. |
| `*`groupName`*` | `xsd:string` | Nom du groupe. |
| `*`permissionType`*` | `xsd:string` | Choix du type d’autorisation. |
| `*`isAllowed`*` | `xsd:boolean` | Détermine si l’autorisation est autorisée. |
| `*`isOverride`*` | `xsd:boolean` | Détermine si l’autorisation remplace une autre. |

