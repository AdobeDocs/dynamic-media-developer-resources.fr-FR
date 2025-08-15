---
description: Renvoie l’historique de publication d’une ressource.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 15%

---

# getAssetPublishHistory{#getassetpublishhistory}

Renvoie l’historique de publication d’une ressource.

Syntaxe

## Types d’utilisateurs autorisés {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-3541bd9914a44b89acfc1d419b560ee6}

**Entrée (getAssetPublishHistoryParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Poignée de l’entreprise avec l’historique de publication de la ressource. |
| AssetHandle | `xsd:string` | Oui | Ressource contenant l’historique de publication que vous souhaitez examiner. |

**Output (getAssetPublishHistoryReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Tableau de l’historique pub | `types:PublishHistoryArray` | Oui | L’historique de publication de la ressource. |

## Exemples {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Cet exemple de code renvoie l’historique de publication d’une ressource. Un actif n’a jamais été publié si le serveur renvoie un tableau vide.

**Demander**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Réponse**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```
