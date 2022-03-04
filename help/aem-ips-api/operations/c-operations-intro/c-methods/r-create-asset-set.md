---
description: Crée un jeu de ressources générique avec une chaîne de définition de jeu brut à publier sur un serveur d’images.
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 10%

---

# createAssetSet{#createassetset}

Crée un jeu de ressources générique avec une chaîne de définition de jeu brut à publier sur un serveur d’images.

Syntaxe

## Types d’utilisateurs autorisés {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-3580b586296e42a5b21426085b1bb72d}

**Entrée (createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Obligatoire </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Gestionnaire de la société qui contiendra le jeu de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Gestionnaire du dossier dans lequel le nouveau jeu de ressources est créé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom de la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant unique créé par le client pour le type de jeu de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Paramètres de la chaîne de définition définie. <p>Ils doivent se résoudre au format spécifié par la visionneuse cible. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Gestion de la ressource qui agit comme miniature de la nouvelle visionneuse d’images. S’il n’est pas spécifié, IPS tente d’utiliser la première ressource d’image référencée par la visionneuse. </td> 
  </tr> 
 </tbody> 
</table>

**Fonctions de substitution pour setDefinition**

Vous pouvez spécifier des fonctions de substitution dans la ligne qui sont résolues lors de la recherche ou de la publication de catalogue. Les chaînes de substitution ont le format `${<substitution_func>}`. Les fonctions disponibles sont énumérées ci-dessous.

>[!NOTE]
>
>Les littéraux de poignée dans les listes de paramètres doivent être entourés de crochets. `([])`. Tout le texte situé en dehors d’une chaîne de substitution est copié dans la chaîne de sortie lors de la résolution.

| **Fonction de substitution** | **Renvoie** |
|---|---|
| `getFilePath([asset_handle>])` | Le Principal chemin d’accès au fichier source de la ressource. |
| `getCatalogId([<asset_handle>])` | ID de catalogue de la ressource. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valeurs des métadonnées de la ressource. |
| `getThumbCatalogId([<asset_handle>])` | ID de catalogue de la ressource (pour les ressources basées sur une image uniquement). ID de catalogue de la ressource de miniature associée (pour les autres ressources). Si aucune ressource de miniature associée n’est disponible, la fonction renvoie une chaîne vide. |

**Exemple de chaîne setDefinition pour un média**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Au moment de la recherche ou de la publication d’un catalogue, ce problème est résolu sur une chaîne similaire à celle-ci :

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Sortie (createAssetSet)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Gestionnaire du jeu de ressources. |

## Exemples {#section-fed53089de824d67ab96cd9103d384b4}

**Request**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**Réponse**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```
