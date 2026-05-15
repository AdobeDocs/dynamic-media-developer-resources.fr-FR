---
description: Restaure les ressources à partir de la corbeille.
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
TQID: 'https://experienceleague.adobe.com/VeC7td4UAm7HX4azZATUoBf-ZLS00aF7OOipZqmVbdw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 11%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

Restaure les ressources à partir de la corbeille.

Syntaxe

## Types d’utilisateurs autorisés {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-200a61d040c94e489a85241b29cd499a}

**Input (restoreAssetsFromTrashParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Le handle vers une entreprise avec les ressources que vous souhaitez restaurer. |
| assetHandleArray | `types:HandleArray` | Oui | Tableau des descripteurs des ressources à restaurer. |

**Output (restoreAssetsFromTrashReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de ressources supprimées de la corbeille. |
| warningCount | `xsd:int` | Oui | Nombre d’avertissements générés lorsque l’opération a tenté de restaurer les ressources à partir de la corbeille. |
| errorCount | `xsd:int` | Oui | Nombre d’erreurs générées lors de la tentative de restauration de ressources à partir de la corbeille. |
| warningDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des avertissements lorsque l’opération a tenté de restaurer les ressources à partir de la corbeille. |
| errorDetailArray | `types:AssetOperationFaultArray` | Non | Tableau de détails associés aux ressources qui ont généré des erreurs lorsque l’opération a tenté de restaurer les ressources à partir de la corbeille. |

## Exemples {#section-98fe0394b0634ca397c395f14f8a9358}

Cet exemple de code restaure les ressources de la corbeille. La réponse indique que l’opération s’est terminée avec succès.

**Requête**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Réponse**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```
