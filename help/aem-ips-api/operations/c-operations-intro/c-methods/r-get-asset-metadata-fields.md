---
description: Renvoie tous les champs de métadonnées, regroupés par type de ressource.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
TQID: 'https://experienceleague.adobe.com/QyDh-64MoS4PmvZGP3iELBrhqs6w8vf3aUBlweOspWU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
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

**Input (getAssetMetadataFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société dont vous souhaitez récupérer les métadonnées. |

**Output (getAssetMetadataFieldsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | Oui | Tableau de champs de métadonnées par type de ressource. |

## Exemples {#section-d79ab85f29144635b0b61416e52f4f3f}

**Requête**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Réponse**

>[!NOTE]
>
>Tronqué pour des raisons de concision.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
