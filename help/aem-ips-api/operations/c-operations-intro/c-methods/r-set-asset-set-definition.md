---
description: Met à jour la définition du jeu pour un jeu de ressources existant.
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,Gestion des ressources
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 6%

---

# setAssetSetDefinition{#setassetsetdefinition}

Met à jour la définition du jeu pour un jeu de ressources existant.

Syntaxe

## Types d’utilisateurs autorisés {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**Entrée (setAssetDefinitionParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Oui | Gestionnaire de l’entreprise avec le jeu de ressources. |
| `*`assetHandle`*` | `xsd:string` | Oui | Gestion des jeux de ressources |
| `*`setDefinition`*` | `xsd:string` | Oui | Chaîne de définition. Voir ci-dessous. |

**Sortie (setAssetSetDefinitionReturn)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Paramètre setDefinition : A propos {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**Fonctions setDefinition**

Spécifiez les fonctions de substitution `setDefinition` en ligne. Ces problèmes sont résolus lors d’une recherche de catalogue ou lors d’une publication. Les chaînes de substitution ont le format `${<substitution_func>}` et comprennent les éléments suivants :

>[!NOTE]
>
>Les littéraux de gestion dans les listes de paramètres doivent être entourés de crochets `([])`. Le texte en dehors d’une chaîne de substitution est copié dans la chaîne de sortie lors de la résolution.

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Fonction de substitution </th> 
   <th colname="col2" class="entry"> Renvoie le </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> chemin d’accès au fichier Principal. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> ID de catalogue. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([  <span class="varname"> asset_handle  </span>],[  <span class="varname"> metadata_field_handle  </span>])  </span> </td> 
   <td colname="col2"> Valeur des métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([  <span class="varname"> asset_handle  </span>])  </span> </td> 
   <td colname="col2"> ID de catalogue. S’applique aux ressources basées sur des images (Image, Vue ajustée, Vue Calque). <p>Pour d’autres ressources, renvoie l’ID de catalogue de la ressource principale (le cas échéant). Si aucune ressource de miniature n’est associée à la ressource, la fonction renvoie une chaîne vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemples de setDefinition**

Cette chaîne de définition de visionneuse de médias :

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

Résout les problèmes suivants au moment de la recherche ou de la publication :

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## Exemples {#section-739b42eec3074cafae285ec015a2d088}

**Request**

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
