---
description: Renvoie tous les champs de métadonnées, regroupés par type de ressource.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

---

# getAssetMetadataFields{#getassetmetadatafields}

Renvoie tous les champs de métadonnées, regroupés par type de ressource.

Syntaxe

## Types d’utilisateurs autorisés {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Entrée (getAssetMetadataFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Handle de l’entreprise dont vous souhaitez récupérer les métadonnées. |

**Output (getAssetMetadataFieldsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | Oui | Tableau des champs de métadonnées, par type de ressource. |

## Exemples {#section-d79ab85f29144635b0b61416e52f4f3f}

**Demander**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Réponse**

>[!NOTE]
>
>Tronquée par souci de concision.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
