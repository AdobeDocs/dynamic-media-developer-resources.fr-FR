---
description: Déplace un fichier vers un dossier spécifique.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---


# moveAsset{#moveasset}

Déplace un fichier vers un dossier spécifique.

Syntaxe

## Types d’utilisateur autorisés {#section-e4f2d2a58132450aa36da6377134211e}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Pose la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Gérez le fichier à déplacer. |
| `*`folderHandle`*` | `xsd:string` | Oui | Accédez au dossier de destination. |

**Sortie (moveAssetReturn)**

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
