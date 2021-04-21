---
description: Supprime les autorisations des ressources sélectionnées.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 15%

---


# removeAssetPermissions{#removeassetpermissions}

Supprime les autorisations des ressources sélectionnées.

Syntaxe

## Types d’utilisateur autorisés {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Entrée (removeAssetPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | La poignée de la société. |
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée de la ressource avec les autorisations à supprimer. |

**Output (removeAssetPermissionsReturn)**

L&#39;API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-238fa7bb091548f5ba72ced11fc92d4f}

Cet exemple de code supprime les autorisations d’un fichier.

**Request**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Réponse**

Aucune
