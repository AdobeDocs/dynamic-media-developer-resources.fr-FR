---
description: Déplace un fichier vers un dossier spécifique.
seo-description: Déplace un fichier vers un dossier spécifique.
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Scene7 Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAsset{#moveasset}

Déplace un fichier vers un dossier spécifique.

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Pose le . |
| ` *`assetHandle`*` | `xsd:string` | Oui | Traitez le fichier à déplacer. |
| ` *`folderHandle`*` | `xsd:string` | Oui | Accédez au dossier de destination. |

**Output (moveAssetReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-78333769f4f14e2886fdf06433c9d2ad}

Cet exemple de code déplace un fichier dans un dossier.

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
