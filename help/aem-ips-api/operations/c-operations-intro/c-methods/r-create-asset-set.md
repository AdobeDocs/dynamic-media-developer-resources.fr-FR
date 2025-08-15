---
title: Créer un jeu de ressources
description: Crée un ensemble de ressources générique avec une chaîne de définition d’ensemble brute à publier sur un serveur d’images.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 5%

---

# Créer un jeu de ressources{#createassetset}

Crée un ensemble de ressources générique avec une chaîne de définition d’ensemble brute à publier sur un serveur d’images.

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
   <td colname="col1"> <span class="codeph"><span class="varname"> CompanyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Poignée de l’entreprise qui contient le jeu de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> La poignée du dossier dans lequel le nouveau jeu de ressources est créé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nom de la ressource. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Sous-type </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Identifiant unique créé par le client pour le type d’ensemble de ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Paramètres de la chaîne de définition du jeu. <p>Ces paramètres doivent être résolus au format spécifié par la visionneuse cible. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Poignée </span> de ressource miniature </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :chaîne </span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Poignée de la ressource qui sert de miniature pour la nouvelle visionneuse d’images. Si cette valeur n’est pas spécifiée, IPS tente d’utiliser la première ressource d’image référencée par la visionneuse. </td> 
  </tr> 
 </tbody> 
</table>

**Fonctions de substitution pour setDefinition**

Vous pouvez spécifier des fonctions de substitution en ligne qui sont résolues lors de la recherche ou de la publication du catalogue. Les chaînes de substitution ont le format `${<substitution_func>}`. Les fonctions disponibles sont décrites ci-dessous.

>[!NOTE]
>
>Les littéraux de handle des listes de paramètres doivent être entourés de crochets `([])`. Tout le texte qui se trouve en dehors d’une chaîne de substitution est copié mot pour mot dans la chaîne de sortie lors de la résolution.

| **Fonction de substitution** | **Renvoie** |
|---|---|
| `getFilePath([asset_handle>])` | Chemin d’accès au fichier source principal de la ressource. |
| `getCatalogId([<asset_handle>])` | ID de catalogue de la ressource. |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | Valeurs de métadonnées de la ressource. |
| `getThumbCatalogId([<asset_handle>])` | ID de catalogue de la ressource (pour les ressources basées sur des images uniquement). ID de catalogue de la ressource miniature associée (pour les autres ressources). Si aucune ressource miniature associée n’est disponible, la fonction renvoie une chaîne vide. |

**Exemple de chaîne Media setDefinition**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

Lors de la recherche catalogue ou de la publication, ce processus est résolu en une chaîne similaire à ce qui suit :

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**Output (createAssetSet)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| assetHandle | `xsd:string` | Oui | Poignée du jeu de ressources. |

## Exemples {#section-fed53089de824d67ab96cd9103d384b4}

**Requête**

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
