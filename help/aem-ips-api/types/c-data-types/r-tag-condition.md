---
description: Définit les conditions de recherche pour les champs de balise.
seo-description: Définit les conditions de recherche pour les champs de balise.
seo-title: TagCondition
solution: Experience Manager
title: TagCondition
topic: Scene7 Image Production System API
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Poignée de champ de balise. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Dépend du type de champ de balise et de l’utilisation du champ value ou valueArray. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Si <span class="codeph"> la valeur</span> est transmise, <span class="codeph"> op</span> doit être la constante de chaîne Correspond à. La condition correspond à tout fichier associé à la valeur de balise. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Si <span class="codeph"> valueArray</span> est transmis, le champ op peut être la constante <span class="codeph"> Correspond à Tout</span> pour les champs de balise à une ou à plusieurs valeurs. Une <span class="codeph"> condition Correspond à n’importe quelle</span> condition correspond à tout fichier associé à au moins une des valeurs de balise dans <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Pour les champs de balise à plusieurs valeurs, le champ op peut être défini sur la constante <span class="codeph"> Correspond à tout</span> avec le champ <span class="codeph"> valueArray</span> . Dans ce cas, la condition ne correspond qu’aux ressources associées à toutes les valeurs de balise dans le <span class="codeph"> tableau</span> de valeurs (éventuellement en plus des autres valeurs de balise). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valeur</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valeur correspondante. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> Plusieurs valeurs correspondantes. </td> 
  </tr> 
 </tbody> 
</table>

