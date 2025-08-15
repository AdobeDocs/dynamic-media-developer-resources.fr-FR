---
description: Définit les autorisations d’une seule ressource à l’aide d’une ressource d’autorisation.
solution: Experience Manager
title: Définir les autorisations des ressources
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# Définir les autorisations des ressources{#setassetpermissions}

Définit les autorisations d’une seule ressource à l’aide d’une ressource d’autorisation.

Assets héritent par défaut des autorisations du dossier parent. Une fois que vous avez défini les autorisations sur une ressource, elle n’hérite plus des autorisations de son parent, sauf si vous appelez `removeAssetPermissions`.

## Types d’utilisateurs autorisés {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e05abbce6453450fb38747101cb5e228}

**Entrée (setAssetPermissonsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | Poignée de l’entreprise qui contient le dossier que vous souhaitez utiliser. |
| AssetHandle | `xsd:string` | Oui | Poignée de dossier. |
| Tableau d’autorisations | `types:PermissionsUpdateArray` | Oui | Tableau d’autorisations. |

**Output (setAssetPermissonsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-38955bc330bb4909b6b06027ef2b143e}

Cet exemple de code définit les autorisations sur une ressource. Il contient le nom de la société et de la ressource, ainsi qu’un tableau d’autorisations.

**Demander**

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
