---
description: Obtient une liste des contextes de publication actifs pour la société spécifiée. Un contexte de publication est considéré comme actif s’il existe au moins un serveur actif défini pour ce contexte.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
TQID: 'https://experienceleague.adobe.com/g337PVX5asvB-o-VQL0XA5XSrgQ0c2vx0xC4-93Dm8E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

Obtient une liste des contextes de publication actifs pour la société spécifiée. Un contexte de publication est considéré comme actif s’il existe au moins un serveur actif défini pour ce contexte.

Syntaxe

## Types d’utilisateurs autorisés {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-a4be4024e55c472fa6728faec9c5e048}

**Input (getActivePublishContextsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant permettant à l’entreprise de rechercher des contextes de publication actifs |

**Output (getActivePublishContextsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| contextArray | `types:StringArray` | Oui | Tableau de contextes de publication actifs, qui peut inclure zéro ou plusieurs valeurs du contexte de publication. |
