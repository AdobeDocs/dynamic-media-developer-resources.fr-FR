---
description: Récupère un type de jeu de propriétés à l’aide d’une poignée vers une société et du nom du type de jeu de propriétés. Il obtient une structure de type avec la poignée pour le type ainsi que le type de propriété.
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 10%

---


# getPropertySetType{#getpropertysettype}

Récupère un type de jeu de propriétés à l’aide d’une poignée vers une société et du nom du type de jeu de propriétés. Il obtient une structure de type avec la poignée pour le type ainsi que le type de propriété.

Syntaxe

## Types d’utilisateur autorisés {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-c9a53400c44744668bd7915f72d2bf3d}

**Entrée (getPropertySetTypeParam)**

| Nom | Type | Obligatoire | Description |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Non | La poignée de la société. Facultatif, car un type de jeu de propriétés peut appartenir à plusieurs sociétés. |
| `*`name`*` | `xsd:string` | Oui | Nom du type de jeu de propriétés. |

**Output (getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:PropertySetType</span> </td> 
   <td colname="col3"> Oui </td> 
   <td colname="col4">La structure de type qui contient un : 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Handle. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Saisissez name. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Type de propriété. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Valeur qui indique si le type autorise plusieurs types de propriétés. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-1b57199415e34a8fa449f864f8895b14}

Cet exemple de code renvoie un type de jeu de propriétés par nom.

**Request**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Réponse**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

