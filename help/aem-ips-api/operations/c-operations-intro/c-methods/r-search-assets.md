---
description: Recherchez des ressources en fonction de vos critères spécifiés.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 12%

---


# searchAssets{#searchassets}

Recherchez des ressources en fonction de vos critères spécifiés.

Syntaxe

## searchAssets: À propos de {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` est la méthode Principale de récupération des ressources IPS. Cette méthode est utilisée à diverses fins, par exemple pour parcourir la hiérarchie de dossiers ou pour trouver un fichier spécifique par nom.

**Taille de réponse**

`searchAssets` renvoie jusqu’à 1 000 actifs en un seul appel. Pour renvoyer jusqu’à 10 000 actifs par appel, limitez les données de réponse à un sous-ensemble des champs `totalRows`, `name`, `handle`, `type` et `subType`. Pour renvoyer des jeux plus volumineux, configurez la pagination avec le paramètre `resultPage`.

**Limiter la taille du fichier de résultats avec responseFieldArray ou excludeFieldArray**

Limitez la taille de votre jeu de données aux paramètres `responseFieldArray` ou `excludFieldArray`. Ces paramètres permettent de réduire l&#39;utilisation de la mémoire et la bande passante et peuvent améliorer les temps de réponse du serveur.

## Types d’utilisateur autorisés {#section-9c4bc41bb8b4493982197eb13c7cdc55}

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
>L’utilisateur doit disposer d’un accès en lecture pour renvoyer des fichiers.

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
   <td colname="col4"> Poignée de la société contenant les ressources à rechercher. </td> 
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
   <td colname="col4"> Permet aux administrateurs de travailler dans le cadre d’un autre groupe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dossier</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Chemin d’accès racine pour la recherche de ressources. Si ce paramètre est omis, le dossier racine de la société est utilisé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolders</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Définissez cette variable sur <span class="codeph"> true</span> pour rechercher des sous-dossiers. </td> 
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
   <td colname="col4"> <p>Choix des modes de correspondance de recherche pour la combinaison des résultats de <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span> et  <span class="codeph"> metadataConditionArray</span>. La valeur par défaut est <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p> <p>Remarque :  Paramètre obsolète. Il est conseillé de ne pas l'utiliser. </p> </p> <p>Tableau de chaînes de mots-clés à faire correspondre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <p>Choix des modes de correspondance de recherche pour la combinaison de <span class="codeph"> correspondances systemFieldCondition</span>. La valeur par défaut est <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:SystemFieldConditionArray</span> </p> </td> 
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
   <td colname="col4"> <p>Tableau des prédicats de recherche de champs de balises. </p> <p>Les prédicats sont combinés en fonction du paramètre <span class="codeph"> tagMatchMode</span>, puis combinés avec tous les termes de <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span> et <span class="codeph"> metadataConditionArray</span> en fonction de <span class="codeph"> conditionMatchMode</span> définie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Rechercher des modes de correspondance pour la combinaison de <span class="codeph"> correspondancesCondition</span> de métadonnées. La valeur par défaut est <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> type:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des conditions de recherche des champs de métadonnées. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des types de fichier à inclure dans la recherche. </td> 
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
   <td colname="col4">Si <span class="codeph"> true</span> et <span class="codeph"> assetSubTypeArray</span> n'est pas vide, seuls les fichiers dont les sous-types se trouvent dans <span class="codeph"> assetSubTypeArray</span> sont renvoyés. Si <span class="codeph"> false</span> (valeur par défaut), les actifs sans sous-type défini sont renvoyés. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Si la valeur est true, les ressources de sous-produits générées lors de l’assimilation d’une ressource Principale, telles que les images de page PDF extraites, sont exclues des résultats de la recherche. Faux par défaut. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Tableau des conditions de génération de ressources de sous-produits à exclure des résultats de la recherche. S’il est présent, ce paramètre remplace le paramètre excludeByproducts. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
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
   <td colname="col4">Indique la page des résultats à renvoyer, en fonction du format de page <span class="codeph"> recordsPerPage</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Choix des champs de tri des fichiers. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> Choix de direction de tri. </td> 
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
| `*`totalRows`*` | `xsd:int` | Non | Nombre de lignes renvoyé par une recherche lorsque les enregistrements par page ne sont pas limités. |
| `*`assetArray`*` | `types:AssetArray` | Non | Fichiers que la recherche renvoie. |

## Exemples {#section-725484cc09b54772a838ad2cc930b94b}

Cet exemple de code recherche des fichiers d’image qui appartiennent à une société spécifique. La réponse est tronquée pour la brièveté.

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

