---
description: Met à jour une visionneuse d’images.
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Visionneuses d’images
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 18%

---

# updateImageSet{#updateimageset}

Met à jour une visionneuse d’images.

Syntaxe

## Paramètres {#section-3be47dbbce474ce78676b05e163492e3}

**Entrée (updateImageSetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de la société qui contient la visionneuse d’images à modifier. |
| `*`assetHandle`*` | `xsd:string` | Oui | La poignée de la visionneuse d’images que vous souhaitez modifier. |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | Non | Réinitialise les membres de la visionneuse d’images. |
| `*`thumbAssetHandle`*` | `xsd:string` | Non | Gestionnaire de la ressource qui agit comme miniature de la visionneuse d’images. |

**Sortie (updateImageSetReturn)**

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
