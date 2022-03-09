---
description: Ajoute une ou plusieurs ressources à un projet.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

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
| companyHandle | `xsd:string` | Oui | Gérer la société associée au projet en cours. |
| projectHandle | `xsd:string` | Oui | Gérez le projet auquel vous ajoutez des ressources. |
| projectHandleArray | `xsd:HandleArray` | Oui | Tableau des ressources que vous ajoutez au projet en cours. |

**Sortie (addProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de ressources ajoutées avec succès. |
| warningCount | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait d’ajouter des ressources à un projet. |
| errorCount | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait d’ajouter des ressources à un projet. |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | Non | Tableau des avertissements générés par les ressources lorsque l’opération tentait de les ajouter à un projet. |
| companyHandle | `xsd:AssetOperationFaultArray` | Non | Tableau des erreurs générées par les ressources lorsque l’opération tentait de les ajouter à un projet. |

## Exemples {#section-bee5be2402f54cb9a3a02cc07def4135}

Cet exemple ajoute une ressource unique (référencée par son nom d’utilisateur) dans un tableau de gestion des ressources à un projet spécifié dans la requête. L’opération s’est terminée avec succès lorsque la réponse `successCount` renvoie `1`.

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
