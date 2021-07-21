---
description: Crée une ressource dérivée d’une ressource d’image Principale existante.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Gestion des ressources
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

Crée une ressource dérivée d’une ressource d’image Principale existante.

Syntaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Les ressources dérivées spécifient des commandes de protocole Image Server qui modifient la représentation de l’image du propriétaire. Le type dérivé `AdjustedView` permet d’appliquer des modifications simples à une seule image (par exemple, en spécifiant un rectangle de recadrage), tandis que le type `LayerView` permet de créer une vue à plusieurs calques qui peut inclure du texte ou des images supplémentaires.

Contrairement à une copie d’image (voir [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), une image dérivée est liée à l’image de son propriétaire. Les modifications apportées à l’image du propriétaire modifient les ressources dérivées associées. La suppression de l’image du propriétaire supprime toutes les images dérivées associées.

## Types d’utilisateurs autorisés {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-5a0dde01cff6454da3646ea805c2be1e}

**Entrée (createDerivedAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de la société qui contient la ressource à partir de laquelle vous dérirez la nouvelle ressource. |
| `*`ownerHandle`*` | `xsd:string` | Oui | Gestion de la ressource d’image Principale à partir de laquelle la nouvelle image sera dérivée. |
| `*`folderHandle`*` | `xsd:string` | Oui | La gestion du dossier dans lequel la nouvelle ressource dérivée sera créée. |
| `*`name`*` | `xsd:string` | Oui | Nom de la ressource dérivée. |
| `*`type`*` | `xsd:string` | Oui | Type de ressource de la nouvelle ressource dérivée : `AdjustedView` ou `LayerView`. |
| `*`urlModifier`*` | `xsd:string` | Non | Commandes de protocole de traitement d’image ou de rendu d’image appliquées *avant* les commandes de requête ou `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Non | Commandes de protocole de traitement d’image ou de rendu d’image appliquées *après* aux commandes de requête ou `urlPostApplyModifier`. |

**Sortie (createDerivedAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Gestion de la ressource dérivée. |

## Exemples {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

L’exemple de code crée une ressource dérivée avec une vue ajustée et `urlModifier` et `urlPostApplyModifier` avec des valeurs arbitraires. La réponse renvoie la poignée à la ressource nouvellement dérivée.

**Request**

```java
<createDerivedAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <ownerHandle>a|943|1|580</ownerHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>ApiDerivedAsset</name>
   <type>AdjustedView</type>
   <urlModifier>modify=this</urlModifier>
   <urlPostApplyModifier>action=awesome</urlPostApplyModifier>
</createDerivedAssetParam>
```

**Réponse**

```java
<createDerivedAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|944|10|2</assetHandle>
</createDerivedAssetReturn>
```
