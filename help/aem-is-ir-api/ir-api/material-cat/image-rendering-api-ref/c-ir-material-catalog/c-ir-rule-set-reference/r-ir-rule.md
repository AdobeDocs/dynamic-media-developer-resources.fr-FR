---
description: Request rule element. Un ou plusieurs sont facultatifs dans l’élément <ruleSet>.
seo-description: Request rule element. Un ou plusieurs sont facultatifs dans l’élément <ruleSet>.
seo-title: règle
solution: Experience Manager
title: règle
topic: Scene7 Image Serving - Image Rendering API
uuid: f7071681-e97e-4081-aeb1-093d2b23041c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# règle{#rule}

Request rule element. Un ou plusieurs éléments sont facultatifs dans l’ `<ruleset>` élément.

## Attributes {#section-aa23349645434db99d46957a96f2e1e1}

`OnMatch="break"|"continue"|"error"` Facultatif. La valeur par défaut est &quot;break&quot;.

` Name=" *`texte`*"` Facultatif. Utilisé pour identifier l’ `<rule>` élément dans les journaux de débogage et les messages d’erreur.

En outre, `<rule>` les éléments peuvent définir n’importe lequel des attributs suivants dans n’importe quelle combinaison. Si elle est spécifiée et que la règle est correctement mise en correspondance, elle remplace les attributs de catalogue correspondants pour cette requête.

<table id="table_AFEFDE61C9ED40019C10D8FE5B16CA23"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut &lt;rule&gt; </p> </th> 
   <th colname="col2" class="entry"> <p>Attribut Catalogue d’images correspondant </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> DefaultPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f" type="reference" format="dita" scope="local"> attribut:DefautPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ErrorImage </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0" type="reference" format="dita" scope="local"> attribute::ErrorImage </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Expiration </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996" type="reference" format="dita" scope="local"> attribut:Expiration </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> MaxPix </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657" type="reference" format="dita" scope="local"> attribut::MaxPix </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> RootUrl </span> </p> </td> 
   <td colname="col2"> <p> <a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402" type="reference" format="dita" scope="local"> attribut:RootUrl </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

Pour plus d’informations, reportez-vous à la description de l’attribut correspondant du catalogue d’images.

L’attribut Expiration remplace uniquement la valeur d’attribut par défaut ; elle est ignorée si une `catalog::Expiration` valeur spécifique s’applique à la requête.

## Données {#section-401b6dfce082490f81229a19b73f2562}

<table id="simpletable_A7E17B52AF754687ACCFFBE747939331"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;substitution&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> &lt;address filter&gt; </span> </p> </td> 
  <td class="stentry"> <p>Facultatif. </p> </td> 
 </tr> 
</table>

## Remarques {#section-a27b91f9a03047c0bb7edc0967fb4216}

Si les deux `<expression>` et `<substitution>` sont spécifiés et que les sous-chaînes capturées ne sont pas utilisées, la première sous-chaîne correspondante est remplacée par `<substitution>`.

Si `<expression>` n’est pas spécifié, tout chemin correspond et `<substitution>` est ajouté à la fin du chemin.

Si `<substitution>` n’est pas spécifié, la sous-chaîne correspondante est supprimée.

Le `<addressfilter>` paramètre est appliqué uniquement lorsqu’une correspondance se produit et avant l’application des règles de  du.
