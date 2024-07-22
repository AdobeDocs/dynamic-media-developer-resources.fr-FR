---
description: Définit les autorisations de dossier.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 13%

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
| companyHandle | `xsd:string` | Oui | Poignée de la société. |
| folderHandle | `xsd:string` | Oui | Poignée de dossier. |
| setChildren | `xsd:boolean` | Oui | Définit des autorisations sur les enfants appartenant au dossier. |
| permissionArray | `types:PermissionUpdateArray` | Oui | Tableau d’autorisations. |

**Output (setFolderPermissionsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-01730da4be874553ab44e3241cdf6357}

Cet exemple de code spécifie un nom d’entreprise, un nom d’utilisateur de dossier et un tableau d’autorisations avec des informations détaillées sur le dossier. Il applique les mêmes autorisations aux enfants du dossier parent.

**Requête**

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
