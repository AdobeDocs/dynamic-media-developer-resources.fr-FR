---
description: Déplace plusieurs fichiers indépendamment les uns des autres. Il effectue cette opération à l’aide du type AssetMove contenu dans le tableau assetMoveArray. Chaque champ AssetMove contient un dossier de destination.
seo-description: Déplace plusieurs fichiers indépendamment les uns des autres. Il effectue cette opération à l’aide du type AssetMove contenu dans le tableau assetMoveArray. Chaque champ AssetMove contient un dossier de destination.
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Scene7 Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAssets{#moveassets}

Déplace plusieurs fichiers indépendamment les uns des autres. Il effectue cette opération à l’aide du type AssetMove contenu dans le tableau assetMoveArray. Chaque champ AssetMove contient un dossier de destination.

Syntaxe

## Types d’utilisateurs autorisés {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-7d47f663474b41cc83439288ac133cc5}

**Input (moveAssetsReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Oui | Poignée vers le avec les ressources à déplacer. |
| ` *`assetMoveArray`*` | `types:AssetMoveArray` | Oui | Tableau de déplacement des ressources. Il contient un fichier et un dossier de destination de fichier. |

**Output (moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Décompte des ressources déplacé avec succès. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nombre de fichiers qui ont généré des avertissements lorsque l’opération a tenté de les déplacer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nombre de fichiers qui ont généré des erreurs lorsque l’opération a tenté de les déplacer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> avertissementDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaultsqui contiennent les éléments suivants : 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Fichiers qui ont déclenché les avertissements. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Codes d'avertissement. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Raison de l'avertissement. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <span class="codeph"></span>AssetOperationFaultsqui contiennent les éléments suivants : 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Fichiers qui ont généré les erreurs. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Codes d’erreur. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Raison des erreurs. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Cet exemple de code déplace les fichiers vers un emplacement spécifique spécifié par le `assetMoveArray`. Le tableau inclut le nom d’utilisateur et le nom d’utilisateur du dossier. La réponse indique que les ressources ont bien été déplacées.

**Request**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Réponse**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

