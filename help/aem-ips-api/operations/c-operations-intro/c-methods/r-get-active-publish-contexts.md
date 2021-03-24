---
description: Obtient une liste de contextes de publication principaux pour la société spécifiée. Un contexte de publication est considéré comme principal s’il existe au moins un serveur principal défini pour ce contexte.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 10%

---


# getActivePublishContext{#getactivepublishcontext}

Obtient une liste de contextes de publication principaux pour la société spécifiée. Un contexte de publication est considéré comme principal s’il existe au moins un serveur principal défini pour ce contexte.

Syntaxe

## Types d’utilisateur autorisés {#section-eb22397744434dfe92a59ffa2883c2e7}

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

**Entrée (getActivePublishContextesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Le handle vers la société à la requête pour les contextes de publication principaux |

**Output (getActivePublishContextesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | Oui | Tableau de principaux contextes de publication, qui peut inclure zéro ou plusieurs valeurs du contexte de publication. |

