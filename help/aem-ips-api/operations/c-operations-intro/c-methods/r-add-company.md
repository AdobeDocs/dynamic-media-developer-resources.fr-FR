---
description: Ajoute une entreprise au système.
solution: Experience Manager
title: addCompany
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2f834fe8-a621-4a41-9473-8ef53294b348
TQID: 'https://experienceleague.adobe.com/rZS2gAVQH1x-TYvW5A9IImc9M7iF5IMCkJzGliVIJxI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 167
ht-degree: 7%

---

# addCompany{#addcompany}

Ajoute une entreprise au système.

Envoie le nom de la société à ajouter au système et indique éventuellement si la société expire.

Lorsque cette opération est appelée, le système obtient un type companyInfo contenant un nom d’entreprise et des champs descriptifs. Si le nom de la société demandée existe déjà dans le système, il renvoie une `ipsApiFault`.

## Types d’utilisateurs autorisés {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-c64a21b72585447880760db9e7a12ccb}

**Input (addCompanyParam)**

<table id="table_AA915BAD2E8E4A1B9719725994309CE8"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Nom de la société à ajouter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> expire </span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:dateTime</span> </p> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Date d’expiration de la société. Indiquez le fuseau horaire avec la requête pour ce champ. Les fuseaux horaires sont adaptés à l’heure centrale. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addCompanyReturn)**

<table id="table_89EBAC0E0FB34793BD843837BB02B518"> 
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
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Gérer le nom et le , le chemin d’accès racine, la date d’expiration et l’heure de la nouvelle entreprise. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#section-4c8f1bb40d154c77a7b410468206e52b}

Cet exemple illustre une demande d’ajout d’une société au système IPS et la réponse détaillant les informations sur la société ajoutée qui sont nécessaires pour effectuer d’autres opérations.

**Requête**

```java {.line-numbers}
<ns1:addCompanyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:addCompanyParam>
```

**Réponse**

```java {.line-numbers}
<ns1:addCompanyReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:addCompanyReturn>
```

