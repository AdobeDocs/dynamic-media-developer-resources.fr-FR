---
description: Met à jour une visionneuse d’images.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
TQID: 'https://experienceleague.adobe.com/b4eYUJJMox5hAC-vQAtOh189M1bP25VcDchnlvAYoHA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 17%

---

# updateImageSet{#updateimageset}

Met à jour une visionneuse d’images.

Syntaxe

## Paramètres {#section-3be47dbbce474ce78676b05e163492e3}

**Input (updateImageSetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société qui contient la visionneuse d’images à modifier. |
| assetHandle | `xsd:string` | Oui | Poignée de la visionneuse d’images à modifier. |
| memberArray | `types:ImageSetMemberUpdateArray` | Non | Réinitialise les membres de la visionneuse d’images. |
| thumbAssetHandle | `xsd:string` | Non | La poignée de la ressource qui agit comme la miniature de la visionneuse d’images. |

**Output (updateImageSetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| séquence |  |  |  |

## Exemples {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Requête**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Réponse**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

