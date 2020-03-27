---
description: Versions disponibles spécifiques aux paramètres régionaux. Renvoie un des versions spécifiques aux paramètres régionaux disponibles de l’ID de catalogue spécifié dans le chemin d’accès à la requête.
seo-description: Versions disponibles spécifiques aux paramètres régionaux. Renvoie un des versions spécifiques aux paramètres régionaux disponibles de l’ID de catalogue spécifié dans le chemin d’accès à la requête.
seo-title: xlate
solution: Experience Manager
title: xlate
topic: Scene7 Image Serving - Image Rendering API
uuid: 4c2370e5-1d46-4242-89bb-a5ce416ef63c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# xlate{#xlate}

Versions disponibles spécifiques aux paramètres régionaux. Renvoie un des versions spécifiques aux paramètres régionaux disponibles de l’ID de catalogue spécifié dans le chemin d’accès à la requête.

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Voir Traduction [des ID d’](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414)objet.

Par exemple :

`xlate.translatedIds=image,image_fr,image_de`

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Default is `s7jsonResponse`.
