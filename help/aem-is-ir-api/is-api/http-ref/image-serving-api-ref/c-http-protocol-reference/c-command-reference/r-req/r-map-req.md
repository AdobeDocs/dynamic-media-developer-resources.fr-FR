---
description: Données de zone cliquable.
solution: Experience Manager
title: carte
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 7%

---

# carte{#map}

Données de zone cliquable.

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encodage</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Renvoie `catalog::Map` sans modification lors de l’interrogation d’une entrée de catalogue simple sans commandes supplémentaires spécifiées (ne sera pas mis à l’échelle vers `catalog::maxPix`).

Si d’autres commandes sont spécifiées dans la requête, une zone cliquable composite est renvoyée, qui est dérivée par la mise à l’échelle, le recadrage, la rotation et la mise en calque de toutes les commandes `catalog::Map` et/ou `map=` incluses dans la requête, tout comme les données de l’image seraient avec `req=img`.

Spécifiez `text` ou omettez le deuxième paramètre pour renvoyer les données de zone cliquable sous la forme d’une chaîne d’élément `HTML <AREA>` avec le type MIME de réponse `text/plain`.

Spécifiez `xml` pour formater la réponse au format XML au lieu de HTML. Le codage du texte peut être spécifié de manière facultative. The default is `UTF-8`.

Renvoie une chaîne vide (ou un élément `<AREA>` vide) si aucune donnée map n’a été trouvée pour les objets de catalogue spécifiés, et/ou si aucun élément `<AREA>` ne reste après le recadrage des images.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.

Voir [Zone cliquable](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
