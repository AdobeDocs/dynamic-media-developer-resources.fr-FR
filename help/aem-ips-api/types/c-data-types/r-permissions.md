---
description: Gère les droits d’accès, de modification, de création ou de suppression de fichiers par groupe.
seo-description: Gère les droits d’accès, de modification, de création ou de suppression de fichiers par groupe.
seo-title: Autorisation
solution: Experience Manager
title: Autorisation
uuid: 3b3580d3-e5bc-42bf-bfbe-ab0ec2dea574
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 6%

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

