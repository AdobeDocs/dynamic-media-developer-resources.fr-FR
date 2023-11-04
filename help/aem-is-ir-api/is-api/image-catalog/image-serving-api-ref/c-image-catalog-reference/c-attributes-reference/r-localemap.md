---
description: Carte de traduction des identifiants. Indique les règles utilisées pour traduire les ID d’image génériques en ID spécifiques aux paramètres régionaux.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# LocaleMap{#localemap}

Carte de traduction des identifiants. Indique les règles utilisées pour traduire les ID d’image génériques en ID spécifiques aux paramètres régionaux.

`*`item`*&#42;['|' *`item`*]`

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

`LocaleMap` fait référence à un `locId` qui peut être mappé à n’importe quel nombre `locSuffix`.

Vide *`locSuffix`* sont autorisées. *`locSuffix`* Les valeurs doivent être triées dans l’ordre dans lequel elles doivent être recherchées. La première correspondance est renvoyée.

Image Serving recherche la variable *`locId`* pour qu’une correspondance non sensible à la casse soit établie avec la variable `locale=` valeur spécifiée dans la requête. Si une correspondance est trouvée, le premier *`locSuffix`* est ajoutée à l’identifiant de catalogue d’origine. Si cette entrée de catalogue existe, elle est utilisée, sinon la suivante *`locSuffix`* est tentée. Si aucun des éléments *`locSuffix`* correspond à une entrée de catalogue, la diffusion d’images renvoie une erreur ou une image par défaut.

Une *`locId`* La valeur correspond à vide et inconnue `locale=` chaînes. Cela permet de définir une règle par défaut pour les paramètres régionaux inconnus.

Lorsque cette option est activée, la traduction des identifiants est appliquée à tous les identifiants référençant les entrées du catalogue d’images et du contenu statique.

## Propriétés {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Un ou plusieurs éléments, séparés par |, où chaque élément se compose de plusieurs valeurs de chaîne séparées par des virgules. *`locId`* et `locale=` sont comparées. Non sensible à la casse.

## Voir aussi {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Aide à la localisation, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
