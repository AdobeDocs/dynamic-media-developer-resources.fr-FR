---
title: DigimarcInfo
description: Infos sur l'image Digimarc. Active l’incorporation Digimarc et spécifie le type de filigrane et toutes les données spécifiques à l’image associées.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---

# DigimarcInfo{#digimarcinfo}

Infos sur l&#39;image Digimarc. Active l’incorporation Digimarc et spécifie le type de filigrane et toutes les données spécifiques à l’image associées.

## Propriétés {#section-62af219e8bac422b8541841221c9ce4f}

Quatre valeurs entières, séparées par des virgules.

`*`type`*, *`flags`*, *`val1`*, *`val2`*`

`*`type`*` active l&#39;incorporation Digimarc et spécifie le type de filigrane :

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type </span> </span> </p> </th> 
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
   <td> <p>De base. </p> </td> 
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
   <td> <p>Années de copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`flags`*` est un champ de bits avec trois valeurs. Définissez le bit 0 pour indiquer le contenu protégé contre la copie, le bit 1 pour indiquer le contenu restreint et le bit 2 pour indiquer le contenu destiné aux adultes :

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> indicateurs </span> </span> </p> </th> 
   <th class="entry"> <p><b> Description </b> </p> </th> 
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
   <td> <p>Restrictions. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protection contre la copie, accès restreint. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Contenu mature. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Copiez du contenu protégé pour adultes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Contenu réservé aux adultes. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>7 <b></b> </p> </td> 
   <td> <p>Contenu protégé par copie, restreint et mature. </p> </td> 
  </tr> 
 </tbody> 
</table>

L&#39;interprétation de `*`val1`*` et `*`val2`*` dépend de `*`type`*` :

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
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
   <td> <p>Première année du droit d’auteur. </p> </td> 
   <td> <p>Deuxième année du droit d’auteur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Par défaut {#section-4bb97e5f79074be89cc691e73449eb43}

Hérité de attribute::DigimarcInfo si le champ n&#39;est pas présent ou est vide.

## Exemples {#section-0f14727a0a2a408781c9df71fed7f42d}

« 0,0,0,0 » désactive le filigrane Digimarc pour cette image.

« 1,5,0,0 » spécifie un filigrane de base avec l’indicateur de contenu pour adultes et protégé contre la copie défini.

« 2 0 4567 0 » indique un filigrane avec un ID d’image.

« 3, 2, 56483, 0 » spécifie un filigrane avec un ID de transaction et l’indicateur de contenu restreint défini.

« 4,0,1998,2001 » précise un filigrane avec des années de droit d&#39;auteur.

## Voir aussi {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
