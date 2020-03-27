---
description: Renvoie des fichiers en fonction d’un tableau de noms de fichiers.
seo-description: Renvoie des fichiers en fonction d’un tableau de noms de fichiers.
seo-title: getAssetsByName
solution: Experience Manager
title: getAssetsByName
topic: Scene7 Image Production System API
uuid: e86b3b16-ad93-4f70-9f59-b72395513c4c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssetsByName{#getassetsbyname}

Renvoie des fichiers en fonction d’un tableau de noms de fichiers.

Syntaxe

## Types d’utilisateurs autorisés {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Renvoie uniquement les fichiers auxquels l’utilisateur a accès en lecture.

## Paramètres {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**Entrée (getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> sociétéHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> La poignée du. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Fournit un accès en tant qu’autre utilisateur. Disponible uniquement pour les administrateurs. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Utilisé pour filtrer selon un groupe spécifique. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Tableau des noms de fichier à récupérer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des types de fichier autorisés pour les fichiers récupérés. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des types de fichier exclus pour les fichiers récupérés. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau de sous-types de ressources autorisés pour les ressources récupérées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Si <span class="codeph"> true</span> et <span class="codeph"> assetSubTypeArray</span> n’est pas vide, seuls les fichiers dont les sous-types se trouvent dans assetSubTypeArray <span class="codeph"></span> sont renvoyés. </p> <p>Si la valeur est <span class="codeph"> false</span>, les fichiers sans sous-type défini sont inclus. </p> <p>The default value is <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Contient un de champs et de sous-champs inclus dans la réponse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Contient un de champs et de sous-champs exclus de la réponse. </td> 
  </tr> 
 </tbody> 
</table>

**Output (getAssetsByNameReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`assetArray`*` | `types:AssetArray` | Non | Tableau de ressources qui correspondent aux critères de filtre. |

## Exemples {#section-3b7447398e574c88aeaf8ca159cc78dd}

Cet exemple de code renvoie deux fichiers de type d’image.

**Request**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**Réponse**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```

