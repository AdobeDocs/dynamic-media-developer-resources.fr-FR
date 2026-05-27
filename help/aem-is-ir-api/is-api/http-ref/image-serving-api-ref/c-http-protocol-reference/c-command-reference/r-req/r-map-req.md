---
title: carte
description: Données de la zone cliquable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
TQID: 'https://experienceleague.adobe.com/Ly1JWjeEyZWUEiyVcv-t-OKf0cp6uuMsbR0B6BE1fhY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 224
ht-degree: 1%

---

# carte{#map}

Données de la zone cliquable.

`req=map[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Encodage de </span></span> <span class="codeph"><span class="varname"></p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Renvoie des `catalog::Map` sans modification lors de l’interrogation d’une entrée de catalogue simple sans commande supplémentaire spécifiée (n’est pas mise à l’échelle sur `catalog::maxPix`).

Si d’autres commandes sont spécifiées dans la requête, une zone cliquable composite est renvoyée. La zone cliquable composite est dérivée par mise à l’échelle, recadrage, rotation et superposition de toutes les commandes de `catalog::Map` et/ou de `map=` incluses dans la requête, comme le seraient les données d’image avec `req=img`.

Spécifiez `text` ou omettez le deuxième paramètre pour pouvoir renvoyer les données de la zone cliquable sous la forme d’une chaîne d’élément de `HTML <AREA>` avec une réponse de type MIME `text/plain`.

Spécifiez `xml` afin de pouvoir formater la réponse au format XML au lieu d’HTML. L’encodage du texte peut être spécifié de manière facultative. La valeur par défaut est `UTF-8`.

Renvoie une chaîne vide (ou un élément de `<AREA>` vide) si aucune donnée de mappage n’a été trouvée pour les objets de catalogue spécifiés et/ou s’il ne reste aucun élément de `<AREA>` après le recadrage des images.

La réponse HTTP peut être mise en cache avec la TTL basée sur `catalog::Expiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

Le `<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.

Voir [Zones cliquables](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
