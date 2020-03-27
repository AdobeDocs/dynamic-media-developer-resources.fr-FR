---
description: Définit les autorisations d’un seul fichier à l’aide d’un fichier d’autorisation.
seo-description: Définit les autorisations d’un seul fichier à l’aide d’un fichier d’autorisation.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Scene7 Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetPermissions{#setassetpermissions}

Définit les autorisations d’un seul fichier à l’aide d’un fichier d’autorisation.

Les ressources héritent par défaut des autorisations de leur dossier parent. Une fois que vous avez défini des autorisations sur un fichier, il n’hérite plus des autorisations de son parent, sauf si vous appelez `removeAssetPermissions`.

## Types d’utilisateurs autorisés {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e05abbce6453450fb38747101cb5e228}

**Input (setAssetPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Identifiant du  qui contient le dossier sur lequel vous souhaitez travailler. |
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée de dossier. |
| ` *`permissionArray`*` | `types:PermissionsUpdateArray` | Oui | tableau des autorisations. |

**Output (setAssetPermissionsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-38955bc330bb4909b6b06027ef2b143e}

Cet exemple de code définit les autorisations sur un fichier. Il contient le  et le nom d’utilisateur du fichier, ainsi qu’un tableau d’autorisations.

**Request**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Réponse**

Aucune
