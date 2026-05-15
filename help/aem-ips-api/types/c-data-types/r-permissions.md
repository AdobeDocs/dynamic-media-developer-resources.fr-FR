---
description: Gère les droits d’accès, de modification, de création ou de suppression des ressources par groupe.
solution: Experience Manager
title: Autorisation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
TQID: 'https://experienceleague.adobe.com/BfB4MGiJFqPkJqL26YSmrhd52KfxhVX5TC-LHxEhevo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 9%

---

# [!DNL Permission]{#permission}

Gère les droits d’accès, de modification, de création ou de suppression des ressources par groupe.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| groupHandle | `xsd:string` | Identifiant du groupe. |
| groupName | `xsd:string` | Nom du groupe. |
| permissionType | `xsd:string` | Choix du type d’autorisation. |
| isAllowed | `xsd:boolean` | Détermine si l’autorisation est autorisée. |
| isOverride | `xsd:boolean` | Détermine si l’autorisation remplace une autre. |
