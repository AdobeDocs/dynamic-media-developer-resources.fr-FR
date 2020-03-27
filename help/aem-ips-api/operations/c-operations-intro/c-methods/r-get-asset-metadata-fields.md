---
description: Renvoie tous les champs de métadonnées, regroupés par type de ressource.
seo-description: Renvoie tous les champs de métadonnées, regroupés par type de ressource.
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
topic: Scene7 Image Production System API
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Identifiant du dont vous souhaitez récupérer les métadonnées. |

**Output (getAssetMetadataFieldsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | Oui | Tableau de champs de métadonnées, par type de fichier. |

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
>Troncée pour la brièveté.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

