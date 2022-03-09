---
description: Définit les autorisations d’une ressource unique à l’aide d’une ressource d’autorisation.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 9%

---

# setAssetPermissions{#setassetpermissions}

Définit les autorisations d’une ressource unique à l’aide d’une ressource d’autorisation.

Les ressources héritent par défaut des autorisations de leur dossier parent. Une fois que vous avez défini des autorisations sur une ressource, elle n’hérite plus des autorisations de son parent, sauf si vous appelez `removeAssetPermissions`.

## Types d’utilisateurs autorisés {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e05abbce6453450fb38747101cb5e228}

**Entrée (setAssetPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Gestionnaire de l’entreprise qui contient le dossier avec lequel vous souhaitez travailler. |
| assetHandle | `xsd:string` | Oui | Poignée de dossier. |
| permissionArray | `types:PermissionsUpdateArray` | Oui | Tableau d’autorisations. |

**Sortie (setAssetPermissionsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-38955bc330bb4909b6b06027ef2b143e}

Cet exemple de code définit des autorisations sur une ressource. Il contient le gestionnaire de l’entreprise et de la ressource, ainsi qu’un tableau d’autorisations.

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
