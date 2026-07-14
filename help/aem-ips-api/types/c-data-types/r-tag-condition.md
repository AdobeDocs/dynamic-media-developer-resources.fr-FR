---
description: Définit les conditions de recherche des champs de balise.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
TQID: 'https://experienceleague.adobe.com/5y2KRE0lZvEuY4wZmcJ-ZrKM5bM9OVwMeSdux9iQl6E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 3%

---

# [!DNL TagCondition]{#tagcondition}

Définit les conditions de recherche des champs de balise.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nom </th> 
   <th colname="col2" class="entry"> Type </th> 
   <th colname="col3" class="entry"> Description </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identifiant du champ de balise. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Dépend du type de champ de balise et si la valeur ou le champ valueArray est utilisé. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Si <span class="codeph"> valeur </span> est transmise, <span class="codeph"> op</span> doit être la constante de chaîne Correspondances. La condition correspond à tout actif associé à la valeur de balise. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Si <span class="codeph"> valueArray</span> est transmis, le champ op peut être la constante <span class="codeph"> MatchesAny</span> pour les champs de balises à une ou plusieurs valeurs. Une condition <span class="codeph"> MatchesAny</span> correspond à tout actif associé à au moins l’une des valeurs de balise dans <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Pour les champs de balise à valeurs multiples, le champ op peut être défini sur la constante <span class="codeph"> MatchesAll</span> avec le champ valueArray</span> <span class="codeph">. Dans ce cas, la condition ne correspond qu’aux ressources associées à toutes les valeurs de balise dans <span class="codeph"> valueArray</span> (éventuellement en plus d’autres valeurs de balise). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> valeur <span class="varname"> </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valeur correspondante. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Plusieurs valeurs correspondantes. </td> 
  </tr> 
 </tbody> 
</table>

