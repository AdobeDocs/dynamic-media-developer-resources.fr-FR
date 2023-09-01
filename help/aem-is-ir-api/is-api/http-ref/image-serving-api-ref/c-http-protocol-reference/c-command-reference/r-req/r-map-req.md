---
title: carte
description: Données de zone cliquable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 9%

---

# carte{#map}

Données de zone cliquable.

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

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

Renvoie `catalog::Map` sans modification lors de l’interrogation d’une entrée de catalogue simple sans commandes supplémentaires spécifiées (ne met pas à l’échelle sur `catalog::maxPix`).

Si d’autres commandes sont spécifiées dans la requête, une zone cliquable composite est renvoyée. La zone cliquable composite est dérivée en effectuant la mise à l’échelle, le recadrage, la rotation et le calquage de toutes les `catalog::Map` et/ou `map=` commandes incluses dans la requête, tout comme les données d’image seraient `req=img`.

Spécifier `text` ou omettez le second paramètre afin de renvoyer les données de zone cliquable sous la forme d’une `HTML <AREA>` chaîne d’élément avec type MIME de réponse `text/plain`.

Spécifier `xml` vous pouvez donc formater la réponse au format XML plutôt que HTML. Le codage du texte peut être spécifié de manière facultative. The default is `UTF-8`.

Renvoie une chaîne vide (ou vide) `<AREA>` ) si aucune donnée map n’a été trouvée pour les objets de catalogue spécifiés, et/ou si aucune donnée n’a été trouvée `<AREA>` restent après avoir recadré les images.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue de `req=` parameter:

`req=...,json [&handler = reqHandler ]`

La variable `<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. The default is `s7jsonResponse`.

Voir [Zones cliquables](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
