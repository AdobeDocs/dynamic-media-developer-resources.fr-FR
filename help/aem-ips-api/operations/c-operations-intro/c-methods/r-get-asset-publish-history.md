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
ht-degree: 17%

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
| companyHandle | `xsd:string` | Oui | Gestion de l’entreprise avec l’historique de publication des ressources. |
| assetHandle | `xsd:string` | Oui | La ressource avec l’historique de publication que vous souhaitez examiner. |

**Sortie (getAssetPublishHistoryReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | Oui | Historique de publication de la ressource. |

## Exemples {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Cet exemple de code renvoie l’historique de publication d’une ressource. Une ressource n’a jamais été publiée si le serveur renvoie un tableau vide.

**Request**

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
