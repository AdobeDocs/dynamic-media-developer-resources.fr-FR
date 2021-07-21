---
description: Obtient les types de jeux de propriétés associés à la société spécifiée ou les types de jeux de propriétés globaux si aucune société n’est spécifiée.
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 7686d30b-e071-4950-8af1-4dd25312ce4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 14%

---

# getPropertySetTypes{#getpropertysettypes}

Obtient les types de jeux de propriétés associés à la société spécifiée ou les types de jeux de propriétés globaux si aucune société n’est spécifiée.

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

**Entrée (getPropertySetTypesParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Non </td> 
   <td colname="col4">Gestion de la société à laquelle les types de jeux de propriétés sont associés. <p>Omit si vous souhaitez renvoyer des types de jeux de propriétés globaux. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (getPropertySetTypesReturn)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | Oui | Tableau de types de jeux de propriétés associés à la société spécifiée ou aux types de jeux de propriétés globaux si aucune société n’a été spécifiée. |

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
