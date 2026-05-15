---
description: Ajoute une ou plusieurs ressources à un projet.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
TQID: 'https://experienceleague.adobe.com/-Oxu138gsQfcPHJ40r8zBEis4AIlNua-gU9DmrGmpF0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 178
ht-degree: 10%

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
| companyHandle | `xsd:string` | Oui | Gérer vers la société associée au projet actuel. |
| projectHandle | `xsd:string` | Oui | Gérez le projet auquel vous ajoutez des ressources. |
| projectHandleArray | `xsd:HandleArray` | Oui | Tableau des ressources que vous ajoutez au projet en cours. |

**Output (addProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de ressources ajoutées avec succès. |
| warningCount | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté d’ajouter des ressources à un projet. |
| errorCount | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté d’ajouter des ressources à un projet. |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | Non | Tableau d’avertissements générés par les ressources lorsque l’opération a tenté de les ajouter à un projet. |
| companyHandle | `xsd:AssetOperationFaultArray` | Non | Tableau d’erreurs générées par des ressources lorsque l’opération a tenté de les ajouter à un projet. |

## Exemples {#section-bee5be2402f54cb9a3a02cc07def4135}

Cet exemple montre comment ajouter une ressource unique (référencée par son descripteur) dans un tableau de descripteurs de ressources à un projet spécifié dans la requête. L’opération s’est terminée avec succès lorsque le `successCount` de réponse renvoie `1`.

**Requête**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Réponse**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
