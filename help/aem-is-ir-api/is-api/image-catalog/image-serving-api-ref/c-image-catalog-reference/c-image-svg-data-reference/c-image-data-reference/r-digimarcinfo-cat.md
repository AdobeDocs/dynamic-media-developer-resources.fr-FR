---
description: Informations sur l'image Digimarc. Active l’incorporation Digimarc et spécifie le type de filigrane et les données associées spécifiques à l’image.
solution: Experience Manager
title: DigimarcInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 12%

---


# DigimarcInfo{#digimarcinfo}

Informations sur l&#39;image Digimarc. Active l’incorporation Digimarc et spécifie le type de filigrane et les données associées spécifiques à l’image.

## Propriétés {#section-62af219e8bac422b8541841221c9ce4f}

Quatre valeurs entières, séparées par des virgules.

`*``*, *``*, *`typeflagsval1`*, *`val2`*`

`*``*` permet l’incorporation de Digimarc et spécifie le type de filigrane :

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
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
   <td> <p>Les années de droit d'auteur. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*``*` flagse un champ de bits avec trois valeurs. Définissez le bit 0 pour indiquer le contenu protégé par copie, le bit 1 pour indiquer le contenu restreint et le bit 2 pour indiquer le contenu adulte :

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> indicateurs</span> </span> </p> </th> 
   <th class="entry"> <p><b>Description</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protégé par copie. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Restreint. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Protégé contre les copies, restreint. </p> </td> 
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
   <td> <p>Contenu protégé par copie, restreint et mature. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;interprétation de `*`val1`*` et `*`val2`*` dépend de `*`type`*` :

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
   <td> <p>Non utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
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

&quot;1,5,0,0&quot; spécifie un filigrane de base avec l’indicateur de contenu pour adultes et protégé par copie défini.

&quot;2,0,4567,0&quot; spécifie un filigrane avec un ID d’image.

&quot;3,2,56483,0&quot; spécifie un filigrane avec un ID de transaction et l’indicateur de contenu restreint défini.

&quot;4,0,1998,2001&quot; spécifie un filigrane avec des années de copyright.

## Voir aussi {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribut::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ,  [attribut::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
