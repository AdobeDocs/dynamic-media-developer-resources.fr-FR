---
description: Supprime les autorisations des ressources sélectionnées.
solution: Experience Manager
title: Supprimer les autorisations des ressources
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 14%

---

# Supprimer les autorisations des ressources{#removeassetpermissions}

Supprime les autorisations des ressources sélectionnées.

Syntaxe

## Types d’utilisateurs autorisés {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Entrée (removeAssetPermissionsParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| CompanyHandle | `xsd:string` | Oui | La poignée de l’entreprise. |
| AssetHandle | `xsd:string` | Oui | Poignée de la ressource pour laquelle vous souhaitez supprimer les autorisations. |

**Output (removeAssetPermissionsReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-238fa7bb091548f5ba72ced11fc92d4f}

Cet exemple de code supprime les autorisations d’une ressource.

**Demander**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Réponse**

Aucune
