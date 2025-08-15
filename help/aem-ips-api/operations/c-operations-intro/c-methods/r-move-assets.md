---
description: Déplace plusieurs ressources indépendamment les unes des autres. Pour ce faire, il utilise le type AssetMove contenu dans le tableau assetMoveArray. Chaque champ AssetMove contient un dossier de destination.
solution: Experience Manager
title: Déplacer les ressources
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 8%

---

# Déplacer les ressources{#moveassets}

Déplace plusieurs ressources indépendamment les unes des autres. Pour ce faire, il utilise le type AssetMove contenu dans le tableau assetMoveArray. Chaque champ AssetMove contient un dossier de destination.

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
| CompanyHandle | `xsd:string` | Oui | Identifiant de la société avec les ressources à déplacer. |
| assetMoveArray | `types:AssetMoveArray` | Oui | Tableau de déplacement de ressources. Il contient une ressource et un dossier de destination de ressources. |

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
   <td colname="col1"> <span class="codeph"><span class="varname"> Compte</span> de succès </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Le nombre de ressources a été déplacé. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nombre de ressources ayant généré des avertissements lors de la tentative de déplacement. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd :int</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4"> Nombre de ressources qui ont généré des erreurs lorsque l’opération a tenté de les déplacer. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> d’événements :AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>qui contiennent les éléments suivants : 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Assets qui a lancé les avertissements. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Codes d’avertissement. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Motif de l’avertissement. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"><span class="varname"> Tableau errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types :AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>contenant : 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Assets qui a généré les erreurs. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Codes d’erreur. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Raison des erreurs. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Cet exemple de code déplace les ressources vers un emplacement spécifique spécifié par la propriété `assetMoveArray` Le tableau comprend le descripteur de ressource et son descripteur de dossier. La réponse indique que les ressources ont été déplacées avec succès.

**Requête**

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
