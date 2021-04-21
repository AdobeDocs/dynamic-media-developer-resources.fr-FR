---
description: Définit les autorisations d’un seul fichier à l’aide d’un fichier d’autorisation.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 8%

---


# setAssetPermissions{#setassetpermissions}

Définit les autorisations d’un seul fichier à l’aide d’un fichier d’autorisation.

Les ressources héritent par défaut des autorisations de leur dossier parent. Une fois que vous avez défini des autorisations sur une ressource, elle n’hérite plus des autorisations de son parent, sauf si vous appelez `removeAssetPermissions`.

## Types d’utilisateur autorisés {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e05abbce6453450fb38747101cb5e228}

**Entrée (setAssetPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Identifiant de la société contenant le dossier que vous souhaitez utiliser. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de dossier. |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | Oui | Tableau des autorisations. |

**Output (setAssetPermissionsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-38955bc330bb4909b6b06027ef2b143e}

Cet exemple de code définit les autorisations sur une ressource. Il contient la société et le nom d’utilisateur du fichier, ainsi qu’un tableau d’autorisations.

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
