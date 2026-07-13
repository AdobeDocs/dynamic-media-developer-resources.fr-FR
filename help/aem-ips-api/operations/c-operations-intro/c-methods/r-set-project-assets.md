---
description: Affectez ou mettez à jour des ressources dans un projet.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
TQID: 'https://experienceleague.adobe.com/J5X6PS7L7YCH6J9ClzAUo24O44fMWxNqPnILckRBbUI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 18%

---

# setProjectAssets{#setprojectassets}

Affectez ou mettez à jour des ressources dans un projet.

Syntaxe

## Types d’utilisateurs autorisés {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Input (setProjectAssetsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyName | `xsd:string` | Oui | Identifiant de la société. |
| projectHandle | `xsd:string` | Oui | Descripteur de projet. |
| assetHandleArray | `types:HandleArray` | Oui | Tableau des descripteurs de ressources à associer au projet. |

**Output (setProjectAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| successCount | `xsd:int` | Oui | Nombre de ressources ajoutées avec succès. |

## Exemples {#section-33c1a909c3dc4aa98da474c23a036596}

Cet exemple de code affecte une ressource à un projet. La requête renvoie un succès de un.

**Requête**

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

