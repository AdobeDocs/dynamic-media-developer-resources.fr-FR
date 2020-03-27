---
description: Obtient les types de jeux de propriétés associés au  de spécifié ou les types de jeux de propriétés globaux si aucun  de n’est spécifié.
seo-description: Obtient les types de jeux de propriétés associés au  de spécifié ou les types de jeux de propriétés globaux si aucun  de n’est spécifié.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Scene7 Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getPropertySetTypes{#getpropertysettypes}

Obtient les types de jeux de propriétés associés au  de spécifié ou les types de jeux de propriétés globaux si aucun  de n’est spécifié.

Syntaxe

## Types d’utilisateurs autorisés {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Input (getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
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
   <td colname="col3"> Non </td> 
   <td colname="col4">poignée du auquel sont associés les types de jeux de propriétés. <p>Omettez si vous souhaitez renvoyer des types de jeux de propriétés globaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getPropertySetTypesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| ` *`typeArray`*` | `types:PropertySetTypeArray` | Oui | Tableau de types de jeux de propriétés associés au  de spécifié ou aux types de jeux de propriétés globaux si aucun  de n’a été spécifié. |

## Exemples {#section-280c406a90864409856aee44d4069a52}

**Request**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**Réponse**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

