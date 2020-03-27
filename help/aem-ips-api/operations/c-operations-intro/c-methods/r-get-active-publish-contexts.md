---
description: Obtient un  de de publication actif  pour l’ de publication spécifiée. Un contexte de publication est considéré comme actif s’il existe au moins un serveur actif défini pour le contexte.
seo-description: Obtient un  de de publication actif  pour l’ de publication spécifiée. Un contexte de publication est considéré comme actif s’il existe au moins un serveur actif défini pour le contexte.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getActivePublishContext{#getactivepublishcontext}

Obtient un  de de publication actif  pour l’ de publication spécifiée. Un contexte de publication est considéré comme actif s’il existe au moins un serveur actif défini pour le contexte.

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

**Input (getActivePublishContextesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Le nom d’utilisateur du  à  pour lejeu de publication actif  |

**Output (getActivePublishContextesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | Oui | Tableau des  de publication actives, qui peut inclure zéro ou plusieurs valeurs du contexte de publication. |

