---
description: Correspondance de traduction des chaînes. Fait référence à un locId qui peut être mappé à n’importe quel nombre de internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---


# LocaleStrMap{#localestrmap}

Correspondance de traduction des chaînes. Fait référence à un locId qui peut être mappé à n’importe quel nombre de internalLocId.

`*``*&#42;['|' *`itemitem`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> élément </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Paramètres régionaux (non sensibles à la casse). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>ID de paramètre régional interne. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` fait référence à un  `locId` qui peut être mappé à n’importe quel nombre de  `internalLocId`.

Une valeur *`locale`* vide correspond à des chaînes vides et inconnues `locale=`. Cela permet de définir une règle par défaut pour les paramètres régionaux inconnus.

Les valeurs *`locId`* vides sont autorisées et sélectionnez *`defaultString`* (*`defaultString`* n’a pas d’identificateur de paramètre régional). *`locId`* sont recherchées dans l’ordre spécifié. La première correspondance est renvoyée.

La traduction des chaînes, lorsqu’elle est activée, est appliquée aux chaînes de texte dans les champs de catalogue d’images suivants :

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Champ de catalogue</b> </td> 
   <td> <b>Elément de chaîne dans le champ</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::ImageSet  </span> </p> </td> 
   <td> <p>Tout sous-élément contenant une chaîne convertible (délimité par toute combinaison de séparateurs ',' ';' ' :' et/ou le début/la fin du champ). </p> <p>Une valeur de couleur <span class="codeph"> 0xrgbb </span> au début d'un champ localisable est exclue de la localisation et transmise sans modification. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::Carte  </span> </p> </td> 
   <td> <p>Toute valeur d’attribut entre guillemets simples ou doublons, à l’exception des valeurs des attributs <span class="codeph"> coords= </span> et <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue::Cibles  </span> </p> </td> 
   <td> <p>Valeur de toute cible <span class="filepath">.*.label </span> et <span class="filepath"> cible.*.userdata </span> propriété. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::UserData  </span> </p> </td> 
   <td> <p>Valeur d’une propriété. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriétés {#section-8505a8525f6948ada3979f68c4081044}

Un ou plusieurs éléments, séparés par |, où chaque élément se compose de plusieurs valeurs de chaîne séparées par des virgules.

## Voir aussi {#section-0c0516e4f83d42d38247308cab9b6708}

Prise en charge de la localisation, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribut::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalogue::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalogue::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalogue::Cibles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalogue: UserData&lt;a 11/>](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
