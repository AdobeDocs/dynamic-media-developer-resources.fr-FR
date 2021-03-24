---
description: Affecter ou mettre à jour des ressources dans un projet.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 18%

---


# setProjectAssets{#setprojectassets}

Affecter ou mettre à jour des ressources dans un projet.

Syntaxe

## Types d’utilisateur autorisés {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Entrée (setProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Oui | Poignée de société. |
| `*`projectHandle`*` | `xsd:string` | Oui | Handle du projet. |
| `*`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de gestionnaires de ressources que vous souhaitez associer au projet. |

**Output (setProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Oui | Nombre de fichiers ajoutés avec succès. |

## Exemples {#section-33c1a909c3dc4aa98da474c23a036596}

Cet exemple de code affecte un fichier à un projet. La requête renvoie un nombre de succès de un.

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

