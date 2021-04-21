---
description: Carte de traduction des identifiants. Indique les règles utilisées pour traduire les identifiants d’image génériques en identifiants spécifiques aux paramètres régionaux.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 1%

---


# LocaleMap{#localemap}

Carte de traduction des identifiants. Indique les règles utilisées pour traduire les identifiants d’image génériques en identifiants spécifiques aux paramètres régionaux.

`*``*&#42;['|' *`itemitem`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> élément</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ID de paramètre régional (non sensible à la casse). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Suffixe régional. </p></td> 
 </tr> 
</table>

`LocaleMap` fait référence à un  `locId` qui peut être mappé à n’importe quel nombre de  `locSuffix`.

Les valeurs *`locSuffix`* vides sont autorisées. *`locSuffix`* doivent être triées dans l’ordre dans lequel elles doivent être recherchées. La première correspondance est renvoyée.

Image Serving recherche les valeurs *`locId`* pour une correspondance insensible à la casse avec la valeur `locale=` spécifiée dans la requête. Si une correspondance est trouvée, la première valeur *`locSuffix`* associée est ajoutée à l’ID de catalogue d’origine. Si cette entrée de catalogue existe, elle est utilisée, sinon la valeur *`locSuffix`* suivante est tentée. Si aucune des valeurs *`locSuffix`* ne correspond à une entrée de catalogue, Image Serving renvoie une erreur ou une image par défaut.

Une valeur *`locId`* vide correspond à des chaînes vides et inconnues `locale=`. Cela permet de définir une règle par défaut pour les paramètres régionaux inconnus.

Lorsqu’elle est activée, la traduction d’ID est appliquée à tous les identifiants référençant les entrées de catalogue d’images et de catalogue de contenu statique.

## Propriétés {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Un ou plusieurs éléments, séparés par |, où chaque élément se compose de plusieurs valeurs de chaîne séparées par des virgules. *`locId`* et  `locale=` sont comparés. Non sensible à la casse.

## Voir aussi {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Prise en charge de la localisation, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribut::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
