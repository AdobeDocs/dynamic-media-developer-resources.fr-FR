---
description: Informations sur l’image Digimarc. Active l’incorporation Digimarc et spécifie le type de filigrane et les données associées spécifiques à l’image.
seo-description: Informations sur l’image Digimarc. Active l’incorporation Digimarc et spécifie le type de filigrane et les données associées spécifiques à l’image.
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
topic: Scene7 Image Serving - Image Rendering API
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DigimarcInfo{#digimarcinfo}

Informations sur l’image Digimarc. Active l’incorporation Digimarc et spécifie le type de filigrane et les données associées spécifiques à l’image.

## Propriétés {#section-62af219e8bac422b8541841221c9ce4f}

Quatre valeurs entières, séparées par des virgules.

` *``*, *``*, *`typeflagsval1`*, *`val2`*`

` *`type`*` active l’incorporation Digimarc et spécifie le type de filigrane :

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span></span> </p> </th> 
   <th class="entry"> <p><b>Type de filigrane</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Aucune </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Basique. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Identifiant de l’image. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>ID de transaction. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Les années de copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

` *`flags`*` est un champ de bits avec trois valeurs. Définissez le bit 0 pour indiquer le contenu protégé contre la copie, le bit 1 pour indiquer le contenu restreint et le bit 2 pour indiquer le contenu adulte :

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> indicateurs</span></span> </p> </th> 
   <th class="entry"> <p><b>Description</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Protégé contre la copie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Restreint. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protégé contre la copie, restreint. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Contenu prêt à l’emploi. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Copiez du contenu protégé pour adultes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Contenu restreint pour adultes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Contenu mûr, protégé contre les copies, restreint et limité. </p> </td> 
  </tr> 
 </tbody> 
</table>

L’interprétation de ` *`val1`*` et ` *`val2`*` dépend du ` *`type`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span></span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span></span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span></span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Identifiant de l’image. </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>ID de transaction. </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Première année de copyright. </p> </td> 
   <td> <p>Deuxième année de copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Par défaut {#section-4bb97e5f79074be89cc691e73449eb43}

Hérité de l’attribut::DigimarcInfo si le champ n’est pas présent ou s’il est vide.

## Exemples {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot; désactive le filigrane Digimarc pour cette image.

&quot;1,5,0,0&quot; spécifie un filigrane de base avec l’indicateur de contenu protégé par copie et pour adulte.

&quot;2,0,4567,0&quot; spécifie un filigrane avec un ID d’image.

&quot;3,2,56483,0&quot; spécifie un filigrane avec un ID de transaction et l’indicateur de contenu restreint défini.

&quot;4,0,1998,2001&quot; spécifie un filigrane avec des années de copyright.

## Voir aussi {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribut::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribut::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
