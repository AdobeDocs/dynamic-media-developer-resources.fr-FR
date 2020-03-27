---
description: Carte de traduction des identifiants. Spécifie les règles utilisées pour traduire les ID d’image génériques en ID spécifiques aux paramètres régionaux.
seo-description: Carte de traduction des identifiants. Spécifie les règles utilisées pour traduire les ID d’image génériques en ID spécifiques aux paramètres régionaux.
seo-title: LocaleMap
solution: Experience Manager
title: LocaleMap
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# LocaleMap{#localemap}

Carte de traduction des identifiants. Spécifie les règles utilisées pour traduire les ID d’image génériques en ID spécifiques aux paramètres régionaux.

` *``*&#42;['|' *`item`*]`

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

`LocaleMap` fait référence à un `locId` qui peut être mappé à n’importe quel nombre de `locSuffix`.

Empty *`locSuffix`* values are permitted. *`locSuffix`* doivent être triées dans l’ordre dans lequel elles doivent être recherchées. La première correspondance est renvoyée.

Le service d’images recherche les *`locId`* valeurs pour une correspondance insensible à la casse avec la `locale=` valeur spécifiée dans la requête. Si une correspondance est trouvée, la première *`locSuffix`* valeur associée est ajoutée à l’ID de catalogue d’origine. Si cette entrée de catalogue existe, elle est utilisée, sinon la *`locSuffix`* valeur suivante est tentée. Si aucune des *`locSuffix`* valeurs ne correspond à une entrée de catalogue, la diffusion d’images renvoie une erreur ou une image par défaut.

Une *`locId`* valeur vide correspond à `locale=` des chaînes vides et inconnues. Cela permet de définir une règle par défaut pour les paramètres régionaux inconnus.

La traduction d’ID, lorsqu’elle est activée, est appliquée à tous les identifiants référençant les entrées de catalogue d’images et de catalogue de contenu statique.

## Propriétés {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Un ou plusieurs éléments, séparés par|, où chaque élément se compose de plusieurs valeurs de chaîne séparées par des virgules. *`locId`* et `locale=` sont comparées. Non sensible à la casse.

## Voir aussi {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Prise en charge des , [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribut::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
