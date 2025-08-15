---
description: Mappage de traduction des chaînes. Fait référence à un locId qui peut être mappé à n’importe quel nombre d’internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

Mappage de traduction des chaînes. Fait référence à un locId qui peut être mappé à n’importe quel nombre d’internalLocId.

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> d’élément </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Paramètre régional (non sensible à la casse). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>Identifiant des paramètres régionaux internes. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` fait référence à un `locId` qui peut être mappé à un nombre illimité de `internalLocId`.

Une valeur de *`locale`* vide correspond à des chaînes de `locale=` vides et inconnues. Cela permet de définir une règle par défaut pour les paramètres régionaux inconnus.

Des valeurs de *`locId`* vides sont autorisées et sélectionnez le *`defaultString`* (le *`defaultString`* ne dispose pas d’un identifiant de paramètre régional). *`locId`* valeurs sont recherchées dans l’ordre spécifié. La première correspondance est renvoyée.

Lorsqu’elle est activée, la traduction de chaînes est appliquée aux chaînes de texte dans les champs de catalogue d’images suivants :

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Champ de catalogue</b> </td> 
   <td> <b>Élément de chaîne dans le champ</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne traduisible (délimitée par n’importe quelle combinaison de séparateurs « , » ; « : » et/ou le début/la fin du champ). </p> <p>Une valeur de couleur de <span class="codeph"> 0xrrggbb </span> au début d’un champ localisable est exclue de la localisation et transmise sans modification. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>Toute valeur d’attribut entre guillemets simples ou doubles, à l’exception des valeurs des attributs coords <span class="codeph">= </span> et Forme <span class="codeph">= </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>Valeur de toute cible <span class="filepath">.*.label </span> et cible <span class="filepath">.Propriété de </span> *.userdata. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>La valeur de n’importe quelle propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8505a8525f6948ada3979f68c4081044}

Un ou plusieurs éléments, séparés par |, où chaque élément se compose de plusieurs valeurs de chaîne séparées par des virgules.

## Voir aussi {#section-0c0516e4f83d42d38247308cab9b6708}

Prise en charge de la localisation, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalog::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalog::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
