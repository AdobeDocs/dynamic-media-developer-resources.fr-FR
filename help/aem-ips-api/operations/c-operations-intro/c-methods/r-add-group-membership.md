---
description: Ajoute un utilisateur à un tableau de groupes.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 14%

---

# addGroupMembership{#addgroupmembership}

Ajoute un utilisateur à un tableau de groupes.

Syntaxe

## Types d’utilisateurs autorisés {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e250f6ddb13646808c6a8860b6442bc5}

**Entrée (addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Gérer l’utilisateur dont vous souhaitez ajouter l’appartenance à un groupe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Tableau de poignées des groupes auxquels l’entreprise doit appartenir. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Sortie (addGroupMembershipParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-f7a1f40c3d7a40ea964b29056c734d81}

Cet exemple ajoute un groupe à une société avec `*`groupHandleArray`*`. Cet exemple n’utilise qu’un seul groupe.

**Request**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Réponse**

Aucune
