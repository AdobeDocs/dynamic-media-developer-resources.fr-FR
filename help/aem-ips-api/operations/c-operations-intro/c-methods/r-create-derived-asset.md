---
description: Crée un nouveau fichier dérivé d’un fichier d’image source Principal existant.
solution: Experience Manager
title: createDerivedAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 8%

---


# createDerivedAsset{#createderivedasset}

Crée un nouveau fichier dérivé d’un fichier d’image source Principal existant.

Syntaxe

<!--<a id="section_FE43FF204ED644C2AC901AF45982E942"></a>-->

Les fichiers dérivés spécifient des commandes de protocole Image Server qui modifient la représentation de l’image du propriétaire. Le type dérivé `AdjustedView` permet d&#39;appliquer des modifications simples à une seule image (en spécifiant, par exemple, un rectangle de recadrage), tandis que le type dérivé `LayerView` permet de créer une vue multicouches qui peut inclure du texte ou des images supplémentaires.

Contrairement à une copie d’image (voir [copyImage](../../../operations/c-operations-intro/c-methods/r-copy-image.md#reference-0785131e690b4ad08be69172023f35d0)), une image dérivée est liée à son image propriétaire. Les modifications apportées à l’image du propriétaire modifient les ressources dérivées associées. La suppression de l’image du propriétaire supprimera toutes les images dérivées associées.

## Types d’utilisateur autorisés {#authorized-user-types}

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
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de la société qui contient la ressource à partir de laquelle vous allez dériver la nouvelle ressource. |
| `*`ownerHandle`*` | `xsd:string` | Oui | Poignée du fichier d’image Principale à partir duquel la nouvelle image sera dérivée. |
| `*`folderHandle`*` | `xsd:string` | Oui | Identifiant du dossier dans lequel la nouvelle ressource dérivée sera créée. |
| `*`name`*` | `xsd:string` | Oui | Nom de l’actif dérivé. |
| `*`type`*` | `xsd:string` | Oui | Type d’actif du nouvel actif dérivé : `AdjustedView` ou `LayerView`. |
| `*`urlModificateur`*` | `xsd:string` | Non | Commandes de protocole de traitement d’image ou de rendu d’image appliquées *avant* les commandes de requête ou `urlPostApplyModifier`. |
| `*`urlPostApplyModificateur`*` | `xsd:string` | Non | Commandes de protocole de traitement d’image ou de rendu d’image appliquées *après* aux commandes de requête ou `urlPostApplyModifier`. |

**Output (createDerivedAssetParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de l’élément dérivé. |

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

