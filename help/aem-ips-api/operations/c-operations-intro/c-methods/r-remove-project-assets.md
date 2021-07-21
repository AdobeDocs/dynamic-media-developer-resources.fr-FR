---
description: Supprime des ressources d’un projet. Ne détruit pas les ressources.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Gestion des ressources
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

Supprime des ressources d’un projet. Ne détruit pas les ressources.

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
| `*`companyHandle`*` | `xsd:string` | Oui | Gestion de l’entreprise avec les ressources que vous souhaitez déplacer. |
| `*`projectHandle`*` | `xsd:string` | Oui | Gestion des ressources du projet que vous souhaitez déplacer. |
| `*`assetHandleArray`*` | `types:HandleArray` | Oui | Tableau de poignées vers les ressources que vous souhaitez déplacer. |

**Sortie (removeProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Oui | Suppression réussie du nombre de ressources. |
| `*`warningCount`*` | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération tentait de supprimer des ressources du projet. |
| `*`errorCount`*` | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération tentait de supprimer des ressources du projet. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des avertissements lorsque l’opération tentait de les supprimer du projet. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Non | Tableau des détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté de les supprimer du projet. |

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
