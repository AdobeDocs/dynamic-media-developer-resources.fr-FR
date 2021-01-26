---
description: Renvoie tous les champs de métadonnées, regroupés par type de ressource.
seo-description: Renvoie tous les champs de métadonnées, regroupés par type de ressource.
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
topic: Dynamic Media Image Production System API
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 20%

---


# getAssetMetadataFields{#getassetmetadatafields}

Renvoie tous les champs de métadonnées, regroupés par type de ressource.

Syntaxe

## Types d’utilisateur autorisés {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société dont vous souhaitez récupérer les métadonnées. |

**Output (getAssetMetadataFieldsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | Oui | Tableau des champs de métadonnées, par type de ressource. |

## Exemples {#section-d79ab85f29144635b0b61416e52f4f3f}

**Request**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Réponse**

>[!NOTE]
>
>Tronqué pour la brièveté.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

