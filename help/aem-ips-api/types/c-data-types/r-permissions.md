---
description: Gère les droits d’accès, de modification, de création ou de suppression des ressources par groupe.
solution: Experience Manager
title: Autorisation
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 8%

---

# Autorisation{#permission}

Gère les droits d’accès, de modification, de création ou de suppression des ressources par groupe.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`groupHandle`*` | `xsd:string` | Poignée de groupe. |
| `*`groupName`*` | `xsd:string` | Nom du groupe. |
| `*`permissionType`*` | `xsd:string` | Choix du type d’autorisation. |
| `*`isAllowed`*` | `xsd:boolean` | Détermine si l’autorisation est autorisée. |
| `*`isOverride`*` | `xsd:boolean` | Détermine si l’autorisation remplace une autre. |
