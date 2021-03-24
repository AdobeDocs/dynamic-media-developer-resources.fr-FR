---
description: Supprime des actifs d’un projet. Ne détruit pas les actifs.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic, SDK/API, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 10%

---


# removeProjectAssets{#removeprojectassets}

Supprime des actifs d’un projet. Ne détruit pas les actifs.

Syntaxe

## Types d’utilisateur autorisés {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-169d8e317417415b87df86242f65710e}

**Entrée (removeProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée vers la société contenant les ressources à déplacer. |
| `*`projectHandle`*` | `xsd:string` | Oui | Poignée des ressources du projet que vous souhaitez déplacer. |
| `*`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées vers les ressources à déplacer. |

**Sortie (removeProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Oui | Le décompte des ressources a été correctement supprimé. |
| `*`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de supprimer des ressources du projet. |
| `*`errorCount`*` | `xsd:int` | Oui | Nombre d&#39;erreurs générées lorsque l&#39;opération tentait de supprimer des ressources du projet. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l&#39;opération a tenté de les supprimer du projet. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des erreurs lorsque l&#39;opération a tenté de les supprimer du projet. |

## Exemples {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Cet exemple de code supprime 2 ressources d&#39;un projet (spécifié par le descripteur de projet).

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

