---
description: Mettez à jour les autorisations de dossier.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 16%

---

# updateFolderPermissions{#updatefolderpermissions}

Mettez à jour les autorisations de dossier.

Syntaxe

## Types d’utilisateurs autorisés {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société. |
| folderHandle | `xsd:string` | Oui | Handle du dossier. |
| updateChildren | `xsd:boolean` | Oui | Détermine s’il faut mettre à jour les enfants avec des autorisations définies pour le dossier de niveau supérieur. |
| updateArray | `types:PermissionUpdateArray` | Oui | Tableau des mises à jour des autorisations à appliquer au dossier. |

**Output (updateFolderPermissionsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-c3fe4d4388674870a3856c35ef66b631}

**Requête**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Réponse**

Aucune
