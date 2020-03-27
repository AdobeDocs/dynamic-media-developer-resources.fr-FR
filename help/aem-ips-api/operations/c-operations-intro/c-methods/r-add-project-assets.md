---
description: Ajoute une ou plusieurs ressources à un projet.
seo-description: Ajoute une ou plusieurs ressources à un projet.
seo-title: addProjectAssets
solution: Experience Manager
title: addProjectAssets
topic: Scene7 Image Production System API
uuid: 48abea17-058e-4469-bb16-0abee8ef5214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addProjectAssets{#addprojectassets}

Ajoute une ou plusieurs ressources à un projet.

Syntaxe

## Types d’utilisateurs autorisés {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-20d498e971b6466298e60c8a77fc32b2}

**Entrée (addProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Traitement du  associé au projet actuel. |
| ` *`projectHandle`*` | `xsd:string` | Oui | Traitez le projet auquel vous ajoutez des ressources. |
| ` *`projectHandleArray`*` | `xsd:HandleArray` | Oui | Tableau des ressources que vous ajoutez au projet actuel. |

**Output (addProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Oui | Nombre de fichiers ajoutés avec succès. |
| ` *`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait d’ajouter des ressources à un projet. |
| ` *`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait d’ajouter des ressources à un projet. |
| ` *`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | Non | Tableau des avertissements générés par les ressources lorsque l’opération tentait de les ajouter à un projet. |
| ` *`companyHandle`*` | `xsd:AssetOperationFaultArray` | Non | Tableau des erreurs générées par les ressources lorsque l’opération tentait de les ajouter à un projet. |

## Exemples {#section-bee5be2402f54cb9a3a02cc07def4135}

Cet exemple montre comment ajouter un seul fichier (référencé par son nom d&#39;utilisateur) dans un tableau de descripteurs de ressources à un projet spécifié dans la requête. L&#39;opération s&#39;est terminée correctement lorsque la réponse `successCount` est renvoyée `1`.

**Request**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Réponse**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

