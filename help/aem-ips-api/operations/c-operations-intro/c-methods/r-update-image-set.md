---
description: Met à jour une visionneuse d’images.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic, SDK/API, visionneuses d’images
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 18%

---


# updateImageSet{#updateimageset}

Met à jour une visionneuse d’images.

Syntaxe

## Paramètres {#section-3be47dbbce474ce78676b05e163492e3}

**Entrée (updateImageSetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant la visionneuse d’images à modifier. |
| `*`assetHandle`*` | `xsd:string` | Ys | Poignée de la visionneuse d’images à modifier. |
| `*`MemberArray`*` | `types:ImageSetMemberUpdateArray` | Non | Réinitialise les membres de la visionneuse d’images. |
| `*`thumbAssetHandle`*` | `xsd:string` | Non | Poignée du fichier qui agit comme miniature pour la visionneuse d’images. |

**Output (updateImageSetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`séquence`*` |  |  |  |

## Exemples {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Request**

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

