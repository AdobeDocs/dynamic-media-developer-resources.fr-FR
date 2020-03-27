---
description: Affectez ou mettez à jour des ressources dans un projet.
seo-description: Affectez ou mettez à jour des ressources dans un projet.
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Scene7 Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setProjectAssets{#setprojectassets}

Affectez ou mettez à jour des ressources dans un projet.

Syntaxe

## Types d’utilisateurs autorisés {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Input (setProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Oui |  poignée. |
| ` *`projectHandle`*` | `xsd:string` | Oui | Gestionnaire de projet. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de ressources que vous souhaitez associer au projet. |

**Output (setProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Oui | Nombre de fichiers ajoutés avec succès. |

## Exemples {#section-33c1a909c3dc4aa98da474c23a036596}

Cet exemple de code affecte un fichier à un projet. La requête renvoie un nombre de succès d’un.

**Request**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Réponse**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

