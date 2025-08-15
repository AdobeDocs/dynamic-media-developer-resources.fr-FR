---
description: Crée une nouvelle ressource dérivée d’une ressource d’image source primaire existante.
solution: Experience Manager
title: Créer une ressource dérivée
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 8%

---

# Créer une ressource dérivée{#createderivedasset}

Crée une nouvelle ressource dérivée d’une ressource d’image source primaire existante.

Syntaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Les ressources dérivées spécifient les commandes du protocole Image Server qui modifient la représentation de l’image propriétaire. Le `AdjustedView` type dérivé permet d’appliquer des modifications simples à une seule image (par exemple, en spécifiant un rectangle de recadrage), tandis que le `LayerView` permet de créer une vue multicouche qui peut inclure du texte ou des images supplémentaires.

Contrairement à une copie d’image (voir [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), une image dérivée est liée à l’image de son propriétaire. Les modifications apportées à l’image propriétaire modifient les ressources dérivées associées. La suppression de l’image propriétaire supprime les images dérivées associées.

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
| CompanyHandle | `xsd:string` | Oui | Handle de la société qui contient la ressource d’où provient la nouvelle ressource. |
| Poignée propriétaire | `xsd:string` | Oui | Poignée de la ressource d’image principale à partir de laquelle la nouvelle image est dérivée. |
| poignée de dossier | `xsd:string` | Oui | Poignée du dossier dans lequel la nouvelle ressource dérivée est créée. |
| nom | `xsd:string` | Oui | Nom de la ressource dérivée. |
| type | `xsd:string` | Oui | Type de ressource de la nouvelle ressource dérivée : `AdjustedView` ou `LayerView`. |
| Modificateur d’url | `xsd:string` | Non | Commandes du protocole de diffusion d’image ou de rendu d’image appliquées *avant* la ou `urlPostApplyModifier` les commandes. |
| urlPostApplyModifier | `xsd:string` | Non | Les commandes du protocole Image Server ou Image Rendering appliquées *après* à la ou `urlPostApplyModifier` aux commandes. |

**Output (createDerivedAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| AssetHandle | `xsd:string` | Oui | Poignée de la ressource dérivée. |

## Exemples {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

L’exemple de code crée une ressource dérivée avec une vue ajustée et `urlModifier` avec `urlPostApplyModifier` des valeurs arbitraires. La réponse renvoie la poignée à la ressource nouvellement dérivée.

**Demander**

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
