---
description: Supprime des fichiers d’un projet. Ne détruit pas les actifs.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

Supprime des fichiers d’un projet. Ne détruit pas les actifs.

Syntaxe

## Types d’utilisateurs autorisés {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-169d8e317417415b87df86242f65710e}

**Entrée (removeProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Poignée vers l’entreprise avec les ressources que vous souhaitez déplacer. |
| Poignée de projet | `xsd:string` | Oui | Poignée des ressources de projet que vous souhaitez déplacer. |
| assetHandleArray | `types:HandleArray` | Oui | Tableau de poignées pour les ressources que vous souhaitez déplacer. |

**Output (removeProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| Compte de succès | `xsd:int` | Oui | Nombre de ressources supprimées avec succès. |
| Nombre d’avertissements | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de supprimer des actifs du projet. |
| Nombre d’erreurs | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de supprimer des actifs du projet. |
| Tableau des détails de l’avertissement | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources qui ont généré des avertissements lorsque l’opération a tenté de les supprimer du projet. |
| Tableau errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associé aux ressources qui ont généré des erreurs lorsque l’opération a tenté de les supprimer du projet. |

## Exemples {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Cet exemple de code supprime 2 ressources d’un projet (spécifiées par le nom de projet).

**Demander**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```
