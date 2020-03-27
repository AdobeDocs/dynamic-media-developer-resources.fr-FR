---
description: Crée un fichier dérivé d’un fichier d’image original existant.
seo-description: Crée un fichier dérivé d’un fichier d’image original existant.
seo-title: createDerivedAsset
solution: Experience Manager
title: createDerivedAsset
topic: Scene7 Image Production System API
uuid: e1f9b690-af34-4da5-a534-c3a8c6b0a8fc
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# createDerivedAsset{#createderivedasset}

Crée un fichier dérivé d’un fichier d’image original existant.

Syntaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Les fichiers dérivés spécifient les commandes du protocole Image Server qui modifient la représentation de l’image du propriétaire. Le type `AdjustedView` dérivé permet d’appliquer des modifications simples à une image unique (par exemple, en spécifiant un rectangle de recadrage), tandis que le `LayerView` permet de créer un multicouche qui peut inclure du texte ou des images supplémentaires.

Contrairement à une copie d’image (voir [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), une image dérivée est liée à son image propriétaire. Les modifications apportées à l’image du propriétaire modifient les fichiers dérivés associés. La suppression de l’image du propriétaire supprimera toutes les images dérivées associées.

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée vers le qui contient le fichier à partir duquel vous allez dériver le nouveau fichier. |
| ` *`ownerHandle`*` | `xsd:string` | Oui | Poignée du fichier image original à partir duquel la nouvelle image sera dérivée. |
| ` *`folderHandle`*` | `xsd:string` | Oui | Identifiant du dossier dans lequel la nouvelle ressource dérivée sera créée. |
| ` *`nom`*` | `xsd:string` | Oui | Nom de la ressource dérivée. |
| ` *`type`*` | `xsd:string` | Oui | Type d’actif du nouvel actif dérivé : `AdjustedView` ou `LayerView`. |
| ` *`urlModificateur`*` | `xsd:string` | Non | Commandes du protocole de traitement d’image ou de rendu d’image appliquées *avant* la ou les `urlPostApplyModifier` commandes de requête. |
| ` *`urlPostApplyModificateur`*` | `xsd:string` | Non | Commandes du protocole de traitement d’image ou de rendu d’image appliquées *après* la requête ou les `urlPostApplyModifier` commandes. |

**Output (createDerivedAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée de la ressource dérivée. |

## Exemples {#section-5d5ea893a1ef4edc8b3a396f1936e8c9}

L’exemple de code crée une ressource dérivée avec une  et `urlModifier` des valeurs ajustées `urlPostApplyModifier` et arbitraires. La réponse renvoie la poignée à la ressource nouvellement dérivée.

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

