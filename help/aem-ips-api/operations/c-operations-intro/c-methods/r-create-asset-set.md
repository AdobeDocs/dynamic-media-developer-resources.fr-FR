---
description: Crée un jeu de fichiers générique avec une chaîne de définition de jeu brut à publier sur un serveur d’images.
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 10%

---


# createAssetSet{#createassetset}

Crée un jeu de fichiers générique avec une chaîne de définition de jeu brut à publier sur un serveur d’images.

Syntaxe

## Types d’utilisateur autorisés {#section-d670d3af552147199b65c7eb847544a3}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée de la société qui contiendra le jeu de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant du dossier dans lequel le nouveau jeu de ressources sera créé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom du fichier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identificateur unique créé par le client pour le type de jeu de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Paramètres de la chaîne de définition de jeu. <p>Elles doivent être résolues selon le format spécifié par la visionneuse de cibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle  </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string  </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Gestion du fichier qui agit comme miniature pour la nouvelle visionneuse d’images. S’il n’est pas spécifié, IPS tente d’utiliser le premier fichier d’image référencé par la visionneuse. </td> 
  </tr> 
 </tbody> 
</table>

**Fonctions de substitution pour setDefinition**

Vous pouvez spécifier des fonctions de substitution dans la ligne qui sont résolues lors de la recherche ou de la publication de catalogue. Les chaînes de substitution ont le format `${<substitution_func>}`. Les fonctions disponibles sont énumérées ci-dessous.

>[!NOTE]
>
>Les littéraux de poignée des listes de paramètres doivent être entourés de crochets `([])`. Tout le texte qui se trouve en dehors d’une chaîne de substitution est copié verbatim dans la chaîne de sortie pendant la résolution.

| **Fonction de substitution** | **Retours** |
|---|---|
| `getFilePath([asset_handle>])` | Principal chemin d’accès au fichier source. |
| `getCatalogId([<asset_handle>])` | ID catalogue de la ressource. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valeurs de métadonnées de la ressource. |
| `getThumbCatalogId([<asset_handle>])` | ID catalogue de la ressource (pour les ressources basées sur une image uniquement). ID catalogue de la ressource miniature associée (pour les autres ressources). Si une ressource miniature associée n’est pas disponible, la fonction renvoie une chaîne vide. |

**Exemple de chaîne de définition de visionneuse de supports**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Lors de la recherche ou de la publication de catalogue, cette erreur est résolue en une chaîne semblable à celle-ci :

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Output (createAssetSet)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Oui | Poignée du jeu de ressources. |

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

