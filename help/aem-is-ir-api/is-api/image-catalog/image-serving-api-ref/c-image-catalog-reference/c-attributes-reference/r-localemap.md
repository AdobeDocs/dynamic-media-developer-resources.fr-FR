---
description: Mappage de traduction d’ID. Indique les règles utilisées pour traduire les identifiants d’image génériques en identifiants spécifiques aux paramètres régionaux.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# LocaleMap{#localemap}

Mappage de traduction d’ID. Indique les règles utilisées pour traduire les identifiants d’image génériques en identifiants spécifiques aux paramètres régionaux.

`*`item`*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> élément</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>Identifiant du paramètre régional (non sensible à la casse). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Suffixe du paramètre régional. </p></td> 
 </tr> 
</table>

`LocaleMap` fait référence à un `locId` qui peut être mappé à un nombre illimité de `locSuffix`.

Des valeurs de *`locSuffix`* vides sont autorisées. *`locSuffix`* valeurs doivent être triées dans l’ordre dans lequel elles doivent être recherchées. La première correspondance est renvoyée.

La diffusion d’images recherche dans les valeurs *`locId`* une correspondance non sensible à la casse avec la valeur `locale=` spécifiée dans la requête. Si une correspondance est trouvée, la première valeur de *`locSuffix`* associée est ajoutée à l’ID de catalogue d’origine. Si cette entrée de catalogue existe, elle est utilisée. Dans le cas contraire, la valeur de *`locSuffix`* suivante est tentée. Si aucune des valeurs *`locSuffix`* ne correspond à une entrée de catalogue, la diffusion d’images renvoie une erreur ou une image par défaut.

Une valeur de *`locId`* vide correspond à des chaînes de `locale=` vides et inconnues. Cela permet de définir une règle par défaut pour les paramètres régionaux inconnus.

La traduction des identifiants, lorsqu’elle est activée, est appliquée à tous les identifiants faisant référence aux entrées du catalogue d’images et du catalogue de contenus statiques.

## Propriétés {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Un ou plusieurs éléments, séparés par |, où chaque élément se compose de plusieurs valeurs de chaîne séparées par des virgules. *`locId`* et `locale=` sont comparés. Non sensible à la casse.

## Voir aussi {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Prise en charge de la localisation, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
