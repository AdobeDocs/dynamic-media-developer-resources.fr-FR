---
description: Correspondance de traduction de chaîne. Fait référence à un locId qui peut être mappé à n’importe quel nombre d’internalLocId.
seo-description: Correspondance de traduction de chaîne. Fait référence à un locId qui peut être mappé à n’importe quel nombre d’internalLocId.
seo-title: LocaleStrMap
solution: Experience Manager
title: LocaleStrMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 44207916-80a6-42cb-8bf1-fcf0f5194c6d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# LocaleStrMap{#localestrmap}

Correspondance de traduction de chaîne. Fait référence à un locId qui peut être mappé à n’importe quel nombre d’internalLocId.

` *``*&#42;['|' *`item`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> élément </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Paramètres régionaux (non sensibles à la casse). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>ID de paramètre régional interne. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` fait référence à un `locId` qui peut être mappé à n’importe quel nombre de `internalLocId`.

Une *`locale`* valeur vide correspond à `locale=` des chaînes vides et inconnues. Cela permet de définir une règle par défaut pour les paramètres régionaux inconnus.

Les *`locId`* valeurs vides sont autorisées et sélectionnez le *`defaultString`* (le *`defaultString`* paramètre régional n’a pas d’identificateur). *`locId`* sont recherchées dans l’ordre spécifié. La première correspondance est renvoyée.

La traduction de chaîne, lorsqu’elle est activée, est appliquée aux chaînes de texte dans les champs de catalogue d’images suivants :

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Champ de catalogue</b> </td> 
   <td> <b>Elément de chaîne dans le champ</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue::ImageSet </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne convertible (délimité par une combinaison quelconque de séparateurs ',' ';' ':' et/ou le /la fin du champ). </p> <p>Une valeur de <span class="codeph"> couleur </span> 0xrrggbb au début d’un champ localisable est exclue du  et transmise sans modification. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::Carte </span> </p> </td> 
   <td> <p>Toute valeur d’attribut entre guillemets simples ou, à l’exception des valeurs des attributs <span class="codeph"> coords= </span> et <span class="codeph"> shape= </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue :: </span> </p> </td> 
   <td> <p>Valeur de tout <span class="filepath"> .*.label </span> et <span class="filepath"> .*.userdata, </span> propriété. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue::UserData </span> </p> </td> 
   <td> <p>Valeur d’une propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8505a8525f6948ada3979f68c4081044}

Un ou plusieurs éléments, séparés par|, où chaque élément se compose de plusieurs valeurs de chaîne séparées par des virgules.

## Voir aussi {#section-0c0516e4f83d42d38247308cab9b6708}

Prise en charge des , [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribut::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalogue::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalogue::Map, catalogue::, catalogue::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md)[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md)[](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
