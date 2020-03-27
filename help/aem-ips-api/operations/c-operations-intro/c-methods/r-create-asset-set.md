---
description: Crée un jeu de fichiers générique avec une chaîne de définition d’ensemble brut à publier sur un serveur d’images.
seo-description: Crée un jeu de fichiers générique avec une chaîne de définition d’ensemble brut à publier sur un serveur d’images.
seo-title: createAssetSet
solution: Experience Manager
title: createAssetSet
topic: Scene7 Image Production System API
uuid: 1e86bd37-511c-4c12-abfd-075053b86f78
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb

---


# createAssetSet{#createassetset}

Crée un jeu de fichiers générique avec une chaîne de définition d’ensemble brut à publier sur un serveur d’images.

Syntaxe

## Types d’utilisateurs autorisés {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-3580b586296e42a5b21426085b1bb72d}

**Input (createAssetSet)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> sociétéHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée du qui contiendra le jeu de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dossierHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant du dossier dans lequel le nouveau jeu de fichiers sera créé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nom </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom du fichier. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sous-type </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant unique créé par le client pour le type de jeu de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Paramètres de la chaîne de définition définie. <p>Elles doivent être résolues selon le format spécifié par le lecteur . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Gestionnaire du fichier qui agit comme miniature pour la nouvelle visionneuse d’images. S’il n’est pas spécifié, IPS tente d’utiliser le premier fichier d’image référencé par la visionneuse. </td> 
  </tr> 
 </tbody> 
</table>

**Fonctions de substitution pour setDefinition**

Vous pouvez spécifier des fonctions de substitution dans la ligne qui sont résolues lors de la recherche ou de la publication de catalogue. Les chaînes de substitution ont le format `${<substitution_func>}`. Les fonctions disponibles sont énumérées ci-dessous.

>[!NOTE]
>
>Les littéraux de poignée dans le paramètre  doivent être entourés de crochets `([])`. Tout le texte qui se trouve en dehors d’une chaîne de substitution est copié verbatim dans la chaîne de sortie pendant la résolution.

| **Fonction de substitution** | **Retours** |
|---|---|
| `getFilePath([asset_handle>])` | Chemin d’accès au fichier maître. |
| `getCatalogId([<asset_handle>])` | ID catalogue de la ressource. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valeurs de métadonnées du fichier. |
| `getThumbCatalogId([<asset_handle>])` | ID catalogue de la ressource (pour les ressources basées sur une image uniquement). ID catalogue de la ressource miniature associée (pour les autres ressources). Si une ressource miniature associée n’est pas disponible, la fonction renvoie une chaîne vide. |

**Exemple de chaîne setDefinition Media**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Au moment de la recherche ou de la publication du catalogue, cette erreur est résolue en une chaîne semblable à celle-ci :

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Output (createAssetSet)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Oui | Poignée du jeu de ressources. |

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

