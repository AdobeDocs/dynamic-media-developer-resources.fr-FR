---
description: Supprime des ressources d’un projet. ne détruit pas les ressources ;
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
TQID: 'https://experienceleague.adobe.com/GHGyYEF5H3Me5jKtkfd15Ok8KEk2hrRuVxrKCF7cZ-E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 10%

---

# removeProjectAssets{#removeprojectassets}

Supprime des ressources d’un projet. ne détruit pas les ressources ;

Syntaxe

## Types d’utilisateurs autorisés {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-169d8e317417415b87df86242f65710e}

**Input (removeProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | La poignée de la société avec les ressources que vous souhaitez déplacer. |
| projectHandle | `xsd:string` | Oui | La poignée des ressources du projet que vous souhaitez déplacer. |
| assetHandleArray | `types:HandleArray` | Oui | Tableau des descripteurs des ressources à déplacer. |

**Output (removeProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de ressources supprimé avec succès. |
| warningCount | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de supprimer des ressources du projet. |
| errorCount | `xsd:int` | Oui | Nombre d’erreurs générées lorsque l’opération a tenté de supprimer des ressources du projet. |
| warningDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des avertissements lorsque l’opération a tenté de les supprimer du projet. |
| errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté de les supprimer du projet. |

## Exemples {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Cet exemple de code supprime 2 ressources d’un projet (spécifiées par le descripteur de projet).

**Requête**

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
