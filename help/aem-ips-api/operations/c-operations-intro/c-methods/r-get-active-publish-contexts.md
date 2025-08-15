---
description: Obtient une liste des contextes de publication actifs pour la société spécifiée. Un contexte de publication est considéré comme actif s’il existe au moins un serveur actif défini pour le contexte.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

Obtient une liste des contextes de publication actifs pour la société spécifiée. Un contexte de publication est considéré comme actif s’il existe au moins un serveur actif défini pour le contexte.

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

**Entrée (getActivePublishContextsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Poignée adressée à la société pour interroger les contextes de publication actifs |

**Output (getActivePublishContextsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau de contexte | `types:StringArray` | Oui | Tableau des contextes de publication actifs, qui peut inclure aucune ou plusieurs valeurs de Publish contexte. |
