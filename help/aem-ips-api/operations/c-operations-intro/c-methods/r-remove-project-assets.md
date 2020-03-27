---
description: Supprime des fichiers d’un projet. Ne détruit pas les fichiers.
seo-description: Supprime des fichiers d’un projet. Ne détruit pas les fichiers.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Scene7 Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeProjectAssets{#removeprojectassets}

Supprime des fichiers d’un projet. Ne détruit pas les fichiers.

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
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée vers le avec les ressources à déplacer. |
| ` *`projectHandle`*` | `xsd:string` | Oui | Identifiant des ressources du projet que vous souhaitez déplacer. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées vers les ressources que vous souhaitez déplacer. |

**Output (removeProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Oui | Le nombre de ressources a été supprimé. |
| ` *`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de supprimer des fichiers du projet. |
| ` *`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de supprimer des fichiers du projet. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l’opération tentait de les supprimer du projet. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des erreurs lorsque l’opération tentait de les supprimer du projet. |

## Exemples {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Cet exemple de code supprime 2 ressources d’un projet (spécifié par le gestionnaire de projet).

**Request**

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

