---
description: Met à jour un jeu de ressources.
seo-description: Met à jour un jeu de ressources.
seo-title: updateAssetSet
solution: Experience Manager
title: updateAssetSet
uuid: e844a395-0ab3-45a7-bcec-8e9e15efc70e
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 18%

---


# updateAssetSet{#updateassetset}

Met à jour un jeu de ressources.

Syntaxe

## Paramètres {#section-d7080ccd97334c94860eb107a3e132b2}

**Entrée (updateAssetSetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société contenant la visionneuse d’images à modifier. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de la visionneuse d’images à modifier. |
| `*`setDefinition`*` | `xsd:string` | Non | Réinitialise les membres de la visionneuse d’images. |
| `*`thumbAssetHandle`*` | `xsd:string` | Non | Poignée du fichier qui agit comme miniature pour la visionneuse d’images. |

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

