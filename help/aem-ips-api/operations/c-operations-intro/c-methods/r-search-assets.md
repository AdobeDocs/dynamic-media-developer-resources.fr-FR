---
description: Recherchez des ressources en fonction de vos critères spécifiés.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 58bd80e4-e9eb-43e4-8508-04e330f0ad26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 12%

---

# searchAssets{#searchassets}

Recherchez des ressources en fonction de vos critères spécifiés.

Syntaxe

## searchAssets : A propos {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` est la méthode Principale de récupération des ressources IPS. Cette méthode est utilisée à diverses fins, par exemple pour parcourir la hiérarchie de dossiers ou rechercher une ressource spécifique par nom.

**Taille de réponse**

`searchAssets` renvoie jusqu’à 1 000 ressources en un seul appel. Pour renvoyer jusqu’à 10 000 ressources par appel, limitez les données de réponse à un sous-ensemble de la variable `totalRows`, `name`, `handle`, `type`, et `subType` champs. Pour renvoyer des jeux plus volumineux, configurez la pagination avec la variable `resultPage` .

**Limiter la taille du fichier de résultat avec responseFieldArray ou excludeFieldArray**

Limitez la taille de votre jeu de données à l’aide de la variable `responseFieldArray` ou `excludFieldArray` paramètres. Ces paramètres réduisent l’utilisation de la mémoire et de la bande passante et peuvent améliorer les temps de réponse du serveur.

## Types d’utilisateurs autorisés {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utilisateur doit disposer d’un accès en lecture pour renvoyer les ressources.

## Paramètres {#section-49aabc0600764f55a8b7017d86ded44f}

**Entrée (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Obligatoire? </th> 
   <th colname="col4" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Gestion de l’entreprise avec les ressources que vous souhaitez rechercher. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Permet aux administrateurs de travailler en tant qu’utilisateur différent. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Permet aux administrateurs de travailler dans un autre groupe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Chemin d’accès racine pour la recherche de ressources. S’il est omis, le dossier racine de l’entreprise est utilisé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Définissez sur . <span class="codeph"> true</span> pour rechercher des sous-dossiers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Choix de l’état de publication. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Choix de l’état de la corbeille. La valeur par défaut est <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Choix des modes de recherche pour la combinaison des résultats de <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>, et <span class="codeph"> metadataConditionArray</span>. La valeur par défaut est <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> <p>Remarque : Paramètre obsolète. Il est conseillé de ne pas l’utiliser. </p> </p> <p>Tableau de chaînes de mots-clés à faire correspondre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Choix des modes de correspondance de recherche à combiner <span class="codeph"> systemFieldCondition</span> correspond à . La valeur par défaut est <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des conditions de champ système. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Constantes de chaîne Modes de correspondance de recherche. La valeur par défaut est <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagConditionArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Tableau de prédicats de recherche de champs de balise. </p> <p>Les prédicats sont combinés en fonction des <span class="codeph"> tagMatchMode</span> puis combinée avec tous les termes de la variable <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span>, et <span class="codeph"> metadataConditionArray</span> selon la variable <span class="codeph"> conditionMatchMode</span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Modes de recherche à combiner <span class="codeph"> metadataCondition</span> correspond à . La valeur par défaut est <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau de conditions de recherche de champs de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des types de ressources à inclure dans la recherche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des types de ressources à exclure de la recherche. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Liste de noms de sous-types à filtrer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">If <span class="codeph"> true</span> et <span class="codeph"> assetSubTypeArray</span> n’est pas vide, seules les ressources dont les sous-types se trouvent dans <span class="codeph"> assetSubTypeArray</span> sont renvoyées. If <span class="codeph"> false</span> (par défaut), les ressources sans sous-type défini sont renvoyées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Si la valeur est true, les sous-produits générés lors de l’ingestion d’une ressource Principale, tels que les images de page de PDF tronquées, sont exclus des résultats de recherche. Faux par défaut. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des conditions de génération de ressources de sous-produits à exclure des résultats de recherche. S’il est présent, ce paramètre remplace le paramètre excludeByproducts . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:chaîne</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Gestion d’un projet contenant les ressources à rechercher. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Nombre maximal de résultats à renvoyer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Spécifie la page de résultats à renvoyer, en fonction de <span class="codeph"> recordsPerPage</span> taille de la page. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Choix des champs de tri des ressources. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Choix de la direction du tri. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Contient une liste de champs et de sous-champs à inclure dans la réponse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Contient une liste de champs et de sous-champs à exclure de la réponse. </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (searchAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| totalRows | `xsd:int` | Non | Nombre de lignes renvoyé par une recherche lorsque les enregistrements par page ne sont pas limités. |
| assetArray | `types:AssetArray` | Non | Ressources renvoyées par la recherche. |

## Exemples {#section-725484cc09b54772a838ad2cc930b94b}

Cet exemple de code recherche des ressources d’image qui appartiennent à une société spécifique. La réponse est tronquée pour la concision.

**Request**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**Réponse**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```
