---
description: Met à jour la définition d’un ensemble de ressources existant.
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
TQID: 'https://experienceleague.adobe.com/zBcrMhG1gXiWobSgAZs9xv1jSt3q6Ej0gYUQQ4R3aU0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 200
ht-degree: 5%

---

# setAssetSetDefinition{#setassetsetdefinition}

Met à jour la définition d’un ensemble de ressources existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Input (setAssetDefinitionParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| companyHandle | `xsd:string` | Oui | Identifiant de la société avec la ressource définie. |
| assetHandle | `xsd:string` | Oui | Descripteur d’ensemble de ressources |
| setDefinition | `xsd:string` | Oui | Chaîne de définition. Voir ci-dessous. |

**Output (setAssetSetDefinitionReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## setDefinition, paramètre : à propos {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**fonctions setDefinition**

Spécifiez `setDefinition` fonctions de substitution en ligne. Ils sont résolus lors d’une recherche de catalogue ou lors de la publication. Les chaînes de substitution sont au format `${<substitution_func>}` et comprennent les éléments suivants :

>[!NOTE]
>
>Les littéraux de gestion dans les listes de paramètres doivent être entourés de crochets `([])`. Le texte en dehors d’une chaîne de substitution est copié dans la chaîne de sortie lors de la résolution.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Fonction de substitution </th> 
   <th colname="col2" class="entry"> Renvoie la de la ressource </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Chemin du fichier de Principal. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Identifiant du catalogue. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>],[ <span class="varname"> metadata_field_handle </span>]) </span> </td> 
   <td colname="col2"> Valeur des métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> Identifiant du catalogue. S’applique aux ressources basées sur des images (image, vue ajustée, vue de calque). <p>Pour les autres ressources, renvoie l’ID de catalogue de la ressource miniature (le cas échéant). Si aucune ressource de pouces n’est associée à la ressource, la fonction renvoie une chaîne vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

**exemples setDefinition**

Cette chaîne de définition de visionneuse de médias :

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Résout les éléments suivants au moment de la recherche ou de la publication :

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Exemples {#section-739b42eec3074cafae285ec015a2d088}

**Requête**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**Réponse**

Aucune

