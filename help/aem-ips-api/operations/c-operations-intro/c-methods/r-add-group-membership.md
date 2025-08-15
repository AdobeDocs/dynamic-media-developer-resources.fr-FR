---
description: Ajoute un utilisateur à un tableau de groupes.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 10%

---

# addGroupMembership{#addgroupmembership}

Ajoute un utilisateur à un tableau de groupes.

Syntaxe

## Types d’utilisateurs autorisés {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Paramètres {#section-e250f6ddb13646808c6a8860b6442bc5}

**Input (addGroupMembershipParam)**

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Non </p> </td> 
   <td colname="col4"> <p>Gérez vers l’utilisateur dont vous souhaitez ajouter l’appartenance à un groupe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Oui </p> </td> 
   <td colname="col4"> <p>Tableau de handles vers les groupes auxquels vous souhaitez que la société appartienne. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (addGroupMembershipParam)**

L’API IPS ne renvoie pas de réponse pour cette opération.

## Exemples {#section-f7a1f40c3d7a40ea964b29056c734d81}

Cet exemple montre comment ajouter un groupe à une société ayant pour propriété groupHandleArray. Cet exemple utilise un seul groupe.

**Requête**

```java {.line-numbers}
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Réponse**

Aucune
