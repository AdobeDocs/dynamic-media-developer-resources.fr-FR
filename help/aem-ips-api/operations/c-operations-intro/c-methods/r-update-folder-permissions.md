---
description: Mettez à jour les autorisations du dossier.
seo-description: Mettez à jour les autorisations du dossier.
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
topic: Scene7 Image Production System API
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateFolderPermissions{#updatefolderpermissions}

Mettez à jour les autorisations du dossier.

Syntaxe

## Types d’utilisateurs autorisés {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-339e6e17c5504e1ea79fbdc05f618050}

**Entrée (updateFolderPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui |  poignée. |
| ` *`folderHandle`*` | `xsd:string` | Oui | Poignée de dossier. |
| ` *`updateChildren`*` | `xsd:boolean` | Oui | Détermine s’il faut mettre à jour les enfants avec des autorisations définies pour le dossier de niveau supérieur. |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | Oui | Le tableau des mises à jour des autorisations que vous souhaitez appliquer au dossier. |

**Output (updateFolderPermissionsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-c3fe4d4388674870a3856c35ef66b631}

**Request**

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
