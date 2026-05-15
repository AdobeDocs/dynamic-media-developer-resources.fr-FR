---
description: Obtient les champs de métadonnées définis par l’utilisateur associés à une ressource.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
TQID: 'https://experienceleague.adobe.com/MA5Y2w4x49b36L6s4PICphm1iamWmVdj-BSMmOQxMdA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 13%

---

# getMetadataFields{#getmetadatafields}

Obtient les champs de métadonnées définis par l’utilisateur associés à une ressource.

Syntaxe

## Types d’utilisateurs autorisés {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-bac949e59c0546429c5786fe422d750d}

**Input (getMetadataFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La gestion de l&#39;entreprise. |
| assetType | `xsd:string` | Oui | Types de ressources à partir desquels obtenir des métadonnées |

**Output (getMetadataFieldsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Expression de code | `Code Phrase` |  |  |

## Exemples {#section-dbfde1483d614b5aac2b491cb32115d7}

Cet exemple de code renvoie des ressources de métadonnées pour le type et l’entreprise spécifiés. La réponse contient un tableau de champs de métadonnées dans un tableau de champs . Toutes les ressources n’ont pas les mêmes métadonnées. L’utilisateur IPS définit le champ de métadonnées de la ressource.

**Requête**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Réponse**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```
