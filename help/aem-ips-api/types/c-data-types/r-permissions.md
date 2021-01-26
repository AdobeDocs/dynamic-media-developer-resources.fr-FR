---
description: Gère les droits d’accès, de modification, de création ou de suppression de fichiers par groupe.
seo-description: Gère les droits d’accès, de modification, de création ou de suppression de fichiers par groupe.
seo-title: Autorisation
solution: Experience Manager
title: Autorisation
topic: Dynamic Media Image Production System API
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

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

