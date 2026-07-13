---
description: Élément de règle de requête. Un ou plusieurs sont facultatifs dans l’élément <ruleset>.
solution: Experience Manager
title: règle
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8f56012c-d01c-489c-9d18-91e256f72012
TQID: 'https://experienceleague.adobe.com/jNaX4-STdjDuKxcSFr5GhjpgB8fiGHrfegR1FxZOFhU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 192
ht-degree: 3%

---

# règle{#rule}

Élément de règle de requête. Un ou plusieurs sont facultatifs dans l’élément `<ruleset>`.

## Attributs {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Facultatif. La valeur par défaut est « break ».

` Name=" *`text`*"` Facultatif. Utilisé pour identifier l’élément `<rule>` dans les journaux de débogage et les messages d’erreur.

En outre, les éléments `<rule>` peuvent définir l’un des attributs suivants dans n’importe quelle combinaison. Si elles sont spécifiées, et que la règle correspond correctement, elles remplacent les attributs de catalogue correspondants pour cette requête.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>attribut &lt;rule&gt; </p> </th> 
   <th colname="col2" class="entry"> <p>Attribut de catalogue d’images correspondant </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attribute::DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attribute::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Expiration </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> attribute::Expiration </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </span> <span class="codeph"> MaxPix </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> attribute::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> attribute::RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations, reportez-vous à la description de l’attribut de catalogue d’images correspondant.

L’attribut Expiration remplace uniquement la valeur d’attribut par défaut ; il est ignoré si une valeur d’`catalog::Expiration` spécifique s’applique à la requête.

## Données {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;expression&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;addressfilter&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
</table>

## Remarques {#section-a27b91f9a03047c0bb7edc0967fb4216}

Si `<expression>` et `<substitution>` sont spécifiés et que les sous-chaînes capturées ne sont pas utilisées, la première sous-chaîne correspondante est remplacée par `<substitution>`.

Si `<expression>` n’est pas spécifié, tout chemin correspond et `<substitution>` est ajouté à la fin du chemin.

Si `<substitution>` n’est pas spécifié, la sous-chaîne correspondante est supprimée.

Le `<addressfilter>` est appliqué uniquement lorsqu’une correspondance se produit et avant l’application des règles de requête.

