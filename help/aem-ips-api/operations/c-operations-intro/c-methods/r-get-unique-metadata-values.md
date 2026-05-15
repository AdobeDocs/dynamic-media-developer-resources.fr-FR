---
description: Obtient des valeurs de champ de métadonnées uniques.
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
TQID: 'https://experienceleague.adobe.com/iDDSEPmoOHPlfCBx2wN9AEM4xlwC-s6SAPKVDUd6iEk'
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
source-wordcount: 57
ht-degree: 24%

---

# getUniqueMetadataValues{#getuniquemetadatavalues}

Obtient des valeurs de champ de métadonnées uniques.

Syntaxe

## Types d’utilisateurs autorisés {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-b9d1413811c24566b6d095701f0f66db}

**Input (getUniqueMetadataValuesParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer vers la société. |
| fieldHandle | `xsd:string` | Non | Gérer le champ de métadonnées. |

**Output (getUniqueMetadataValuesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| valeurs | `type:StringArray` |  |  |

## Exemples {#section-440f3bc3e5be436cb6ec26117d05f476}

Cet exemple de code utilise un descripteur de champ pour renvoyer des valeurs de métadonnées spécifiques.

**Requête**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**Réponse**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```
