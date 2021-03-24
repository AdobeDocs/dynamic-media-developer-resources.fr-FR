---
description: Renvoie des informations sur la société spécifiée, y compris le nom d’utilisateur de la société, le nom de la société, le chemin d’accès racine et la date d’expiration. Vous devez spécifier companyHandle ou companyName dont vous souhaitez récupérer les informations.
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 10%

---


# getCompanyInfo{#getcompanyinfo}

Renvoie des informations sur la société spécifiée, y compris le nom d’utilisateur de la société, le nom de la société, le chemin d’accès racine et la date d’expiration. Vous devez spécifier companyHandle ou companyName dont vous souhaitez récupérer les informations.

Syntaxe

## Types d’utilisateur autorisés {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-7dec8871c89a414c9f066adade1831d8}

**Entrée (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> ou <span class="codeph"> <span class="varname"> companyName</span> </span> est requis. </p> </td> 
   <td colname="col4"> <p>Poignée de la société dont vous voulez obtenir les informations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> ou <span class="codeph"> <span class="varname"> companyName</span> </span> est requis. </p> </td> 
   <td colname="col4"> <p>Nom de la société dont vous souhaitez obtenir les informations. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom </p> </th> 
   <th colname="col2" class="entry"> <p>Type </p> </th> 
   <th colname="col3" class="entry"> <p>Obligatoire </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> type:Société</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Traitement et autres informations descriptives sur la société. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Cet exemple de code renvoie toutes les informations relatives à une société à l’aide d’un nom de société et d’un nom d’utilisateur. Elle renvoie des données similaires à la réponse reçue lors de la création d’une société.

**Request**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Réponse**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

