---
description: Déplace une ressource vers un dossier spécifique.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 17%

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

**Entrée (moveAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gérer la société. |
| assetHandle | `xsd:string` | Oui | Gérez la ressource à déplacer. |
| folderHandle | `xsd:string` | Oui | Gérer vers le dossier de destination. |

**Sortie (moveAssetReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-78333769f4f14e2886fdf06433c9d2ad}

Cet exemple de code déplace une ressource vers un dossier.

**Request**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Réponse**

Aucune
