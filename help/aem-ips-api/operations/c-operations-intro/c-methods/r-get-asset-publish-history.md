---
description: Renvoie l’historique de publication d’un fichier.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 16%

---


# getAssetPublishHistory{#getassetpublishhistory}

Renvoie l’historique de publication d’un fichier.

Syntaxe

## Types d’utilisateur autorisés {#section-3b9d6a129093458fa8890139a2718912}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société avec l’historique de publication des ressources. |
| `*`assetHandle`*` | `xsd:string` | Oui | Ressource dont vous souhaitez examiner l’historique de publication. |

**Output (getAssetPublishHistoryReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | Oui | Historique de publication de la ressource. |

## Exemples {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Cet exemple de code renvoie l’historique de publication d’un fichier. Un fichier n&#39;a jamais été publié si le serveur renvoie une baie vide.

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

