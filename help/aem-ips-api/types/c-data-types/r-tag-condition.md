---
description: Définit les conditions de recherche pour les champs de balise.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 7%

---


# TagCondition{#tagcondition}

Définit les conditions de recherche pour les champs de balise.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Poignée de champ de balise. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Dépend du type de champ de balise et de l’utilisation du champ value ou valueArray. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Si <span class="codeph"> valeur</span> est transmise, <span class="codeph"> op</span> doit être la constante de chaîne Correspond à. La condition correspond à tout actif associé à la valeur de balise. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Si <span class="codeph"> valueArray</span> est transmis, le champ op peut être la constante <span class="codeph"> MatchesAny</span> pour les champs de balise à une ou plusieurs valeurs. Une condition <span class="codeph"> Correspond à </span> correspond à toute ressource associée à au moins une des valeurs de balise dans <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Pour les champs de balise à plusieurs valeurs, le champ op peut être défini sur la constante <span class="codeph"> Correspond à </span> avec le champ <span class="codeph"> valueArray</span>. Dans ce cas, la condition correspond uniquement aux actifs associés à toutes les valeurs de balise dans <span class="codeph"> valueArray</span> (éventuellement en plus des autres valeurs de balise). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
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

