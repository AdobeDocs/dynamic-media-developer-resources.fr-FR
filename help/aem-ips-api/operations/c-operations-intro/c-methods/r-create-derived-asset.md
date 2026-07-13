---
description: Crée une ressource dérivée d’une ressource d’image source principale existante.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: a3b20a8a-ed0d-40be-9a8c-41ba09b1d724
TQID: 'https://experienceleague.adobe.com/zREQqRBLpYJ30WoTEa2cmVplhQAlcqoBgzRIsMAy5sg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 259
ht-degree: 8%

---

# createDerivedAsset{#createderivedasset}

Crée une ressource dérivée d’une ressource d’image source principale existante.

Syntaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Les ressources dérivées spécifient les commandes de protocole du serveur d’images qui modifient la représentation de l’image du propriétaire. Le type dérivé de `AdjustedView` permet d’appliquer des modifications simples à une seule image (par exemple, en spécifiant un rectangle de recadrage), tandis que le `LayerView` permet de créer un affichage multicouche qui peut inclure du texte ou des images supplémentaires.

Contrairement à une copie d’image (voir [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), une image dérivée est liée à son image propriétaire. Les modifications apportées à l’image du propriétaire modifient les ressources dérivées associées. La suppression de l’image du propriétaire supprime toutes les images dérivées associées.

## Types d’utilisateurs autorisés {#authorized-user-types}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-5a0dde01cff6454da3646ea805c2be1e}

**Input (createDerivedAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société qui contient la ressource à partir de laquelle vous obtenez la nouvelle ressource. |
| ownerHandle | `xsd:string` | Oui | Pointez sur la ressource d’image principale à partir de laquelle la nouvelle image est dérivée. |
| folderHandle | `xsd:string` | Oui | La poignée du dossier dans lequel la nouvelle ressource dérivée est créée. |
| nom | `xsd:string` | Oui | Nom de la ressource dérivée. |
| type | `xsd:string` | Oui | Type de ressource de la nouvelle ressource dérivée : `AdjustedView` ou `LayerView`. |
| urlModifier | `xsd:string` | Non | Commandes de protocole de diffusion ou de rendu d’image appliquées *avant* les commandes request ou `urlPostApplyModifier`. |
| urlPostApplyModifier | `xsd:string` | Non | Commandes de protocole de diffusion ou de rendu d’image appliquées *après* aux commandes request ou `urlPostApplyModifier`. |

**Output (createDerivedAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetHandle | `xsd:string` | Oui | Poignée de la ressource dérivée. |

## Exemples {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

L’exemple de code crée une ressource dérivée avec une vue et une `urlModifier` ajustées, et `urlPostApplyModifier` avec des valeurs arbitraires. La réponse renvoie la poignée à la ressource nouvellement dérivée.

**Requête**

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

