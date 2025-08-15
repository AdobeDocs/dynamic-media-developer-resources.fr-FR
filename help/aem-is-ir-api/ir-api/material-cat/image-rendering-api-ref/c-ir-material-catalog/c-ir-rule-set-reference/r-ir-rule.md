---
description: Requête d’élément de règle. Un ou plusieurs sont facultatifs dans <ruleset> l’élément.</ruleset>
solution: Experience Manager
title: règle
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# règle{#rule}

Requête d’élément de règle. Un ou plusieurs sont facultatifs dans l’élément `<ruleset>` .

## Attributs {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Optionnel. La valeur par défaut est « break ».

` Name=" *`texte`*"` Facultatif. Utilisé pour identifier l’élément dans les `<rule>` journaux de débogage et les messages d’erreur.

En outre, `<rule>` Elements peut définir l’un des attributs suivants dans n’importe quelle combinaison. S’ils sont spécifiés et que la règle est correctement mise en correspondance, ils remplacent les attributs de catalogue correspondants pour cette demande.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>&lt;rule&gt; attribut&lt;/rule&gt; </p> </th> 
   <th colname="col2" class="entry"> <p>Attribut de catalogue d’images correspondant </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Pix par défaut </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attribut ::D efautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Image erronée </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attribute ::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Expiration </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> attribute ::Expiration </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> attribut ::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> attribut ::RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Reportez-vous à la description de l’attribut de catalogue d’images correspondant pour plus de détails.

L’attribut Expiration remplace uniquement la valeur d’attribut par défaut ; Elle est ignorée si une valeur spécifique `catalog::Expiration` s’applique à la demande.

## Données {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">&lt;expression&gt; </span>&lt;/expression&gt; </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">&lt;substitution&gt; </span>&lt;/substitution&gt; </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">&lt;addressfilter&gt; </span>&lt;/addressfilter&gt; </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
</table>

## Remarques {#section-a27b91f9a03047c0bb7edc0967fb4216}

Si les deux `<expression>` et `<substitution>` sont spécifiées et que les sous-chaînes capturées ne sont pas utilisées, la première sous-chaîne correspondante est remplacée par `<substitution>`.

Si `<expression>` n’est pas spécifié, l’un des chemins d’accès correspond et `<substitution>` est ajouté à la fin du chemin.

Si `<substitution>` n’est pas spécifiée, la sous-chaîne correspondante est supprimée.

L’objet `<addressfilter>` est appliqué uniquement en cas de correspondance et avant l’application des règles de requête.
