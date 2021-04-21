---
description: Met à jour les autorisations de ressources.
solution: Experience Manager
title: updateAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

---


# updateAssetPermissions{#updateassetpermissons}

Met à jour les autorisations de ressources.

Syntaxe

## Types d’utilisateur autorisés {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-392cb3076cf84790a32fd913f2b111a3}

**Entrée (updateAssetPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Poignée de société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de ressource. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Oui | Autorisations que vous souhaitez appliquer à la ressource. |

**Output (updateAssetPermissionsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Request**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Réponse**

Aucune
