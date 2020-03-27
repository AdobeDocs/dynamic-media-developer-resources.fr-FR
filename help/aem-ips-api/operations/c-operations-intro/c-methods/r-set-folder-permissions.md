---
description: Définit les autorisations de dossier.
seo-description: Définit les autorisations de dossier.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Scene7 Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setFolderPermissions{#setfolderpermissions}

Définit les autorisations de dossier.

Syntaxe

## Types d’utilisateurs autorisés {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-2a41135054954396b40f1228f2e63b42}

**Input (setFolderPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`folderHandle`*` | `xsd:string` | Oui | Poignée de dossier. |
| ` *`setChildren`*` | `xsd:boolean` | Oui | Définit les autorisations sur les enfants qui appartiennent au dossier. |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` | Oui | tableau des autorisations. |

**Output (setFolderPermissionsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-01730da4be874553ab44e3241cdf6357}

Cet exemple de code spécifie un , un gestionnaire de dossier et un tableau d’autorisations contenant des informations détaillées sur le dossier. Il applique les mêmes autorisations aux enfants du dossier parent.

**Request**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Réponse**

Aucune
