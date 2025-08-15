---
description: Renvoie des informations sur la société spécifiée, notamment le descripteur de société, le nom de la société, le chemin racine et la date d’expiration. Vous devez spécifier companyHandle ou companyName dont vous souhaitez récupérer les informations.
solution: Experience Manager
title: getCompanyInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72bd223b-c99a-48a3-9c0a-d1af392d904c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 7%

---

# getCompanyInfo{#getcompanyinfo}

Renvoie des informations sur la société spécifiée, notamment le descripteur de société, le nom de la société, le chemin racine et la date d’expiration. Vous devez spécifier companyHandle ou companyName dont vous souhaitez récupérer les informations.

Syntaxe

## Types d’utilisateurs autorisés {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Paramètres {#section-7dec8871c89a414c9f066adade1831d8}

**Input (getCompanyInfoParam)**

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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> CompanyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>companyHandle <span class="codeph"><span class="varname"> </span> </span> ou <span class="codeph"> <span class="varname"> companyName</span> </span> est requis. </p> </td> 
   <td colname="col4"> <p>Pseudo de l’entreprise dont vous souhaitez obtenir les informations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Nom de</span> la société </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd :chaîne</span> </p> </td> 
   <td colname="col3"> <p>companyHandle <span class="codeph"><span class="varname"> </span> </span> ou <span class="codeph"> <span class="varname"> companyName</span> </span> est requis. </p> </td> 
   <td colname="col4"> <p>Le nom de l’entreprise dont vous souhaitez obtenir les informations. </p> </td> 
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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> Infos sur l’entreprise</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types :Société</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Poignée et autres informations descriptives sur l’entreprise. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Cet exemple de code renvoie toutes les informations sur une société à l’aide d’un nom et d’un pseudonyme de société. Elle renvoie des données similaires à la réponse reçue lors de la création d’une société.

**Demander**

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
