---
description: Met à jour un jeu de ressources.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 22%

---

# updateAssetSet{#updateassetset}

Met à jour un jeu de ressources.

Syntaxe

## Paramètres {#section-d7080ccd97334c94860eb107a3e132b2}

**Entrée (updateAssetSetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de la société qui contient la visionneuse d’images à modifier. |
| assetHandle | `xsd:string` | Oui | La poignée de la visionneuse d’images que vous souhaitez modifier. |
| setDefinition | `xsd:string` | Non | Réinitialise les membres de la visionneuse d’images. |
| thumbAssetHandle | `xsd:string` | Non | Gestionnaire de la ressource qui agit comme miniature de la visionneuse d’images. |

**Sortie (updateAssetSetReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
|  |  |  |  |

## Exemples {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Request**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Réponse**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
