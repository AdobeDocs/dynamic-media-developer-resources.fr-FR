---
description: Restaure les fichiers à partir de la corbeille.
seo-description: Restaure les fichiers à partir de la corbeille.
seo-title: restoreAssetsFromTrash
solution: Experience Manager
title: restoreAssetsFromTrash
topic: Scene7 Image Production System API
uuid: f7424d4c-7807-4de9-ad0c-f96364bf7b82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 12%

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

Restaure les fichiers à partir de la corbeille.

Syntaxe

## Types d’utilisateur autorisés {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-200a61d040c94e489a85241b29cd499a}

**Entrée (restoreAssetsFromTrashParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée d’une société contenant les ressources à restaurer. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées pour les ressources à restaurer. |

**Output (restoreAssetsFromTrashReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Oui | Nombre de fichiers supprimés de la corbeille. |
| ` *`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de restaurer des ressources à partir de la corbeille. |
| ` *`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lors de la tentative de restauration de fichiers à partir de la corbeille. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l’opération tentait de restaurer des ressources à partir de la corbeille. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux actifs qui ont généré des erreurs lorsque l’opération tentait de restaurer des actifs à partir de la corbeille. |

## Exemples {#section-98fe0394b0634ca397c395f14f8a9358}

Cet exemple de code restaure les fichiers de la corbeille. La réponse indique que l&#39;opération a réussi.

**Request**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Réponse**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

