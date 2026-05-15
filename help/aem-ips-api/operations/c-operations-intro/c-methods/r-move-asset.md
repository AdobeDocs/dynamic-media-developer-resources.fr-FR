---
description: Déplace une ressource vers un dossier spécifique.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
TQID: 'https://experienceleague.adobe.com/-3pTSenps7g41lho728JLME6EwS2xlYLBfJnuAF6DXY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 14%

---

# moveAsset{#moveasset}

Déplace une ressource vers un dossier spécifique.

Syntaxe

## Types d’utilisateurs autorisés {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Input (moveAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer vers la société. |
| assetHandle | `xsd:string` | Oui | Gérez la ressource à déplacer. |
| folderHandle | `xsd:string` | Oui | Gérer vers le dossier de destination. |

**Output (moveAssetReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-78333769f4f14e2886fdf06433c9d2ad}

Cet exemple de code déplace une ressource vers un dossier.

**Requête**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Réponse**

Aucune
