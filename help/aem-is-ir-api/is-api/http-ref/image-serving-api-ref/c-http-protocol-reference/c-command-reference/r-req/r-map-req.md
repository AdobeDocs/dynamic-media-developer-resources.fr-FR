---
description: Données de zone cliquable.
solution: Experience Manager
title: carte
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
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
  <td class="stentry"> <p>Identificateur de requête unique. </p></td> 
 </tr> 
</table>

Renvoie `catalog::Map` sans modification lors de l&#39;interrogation d&#39;une entrée de catalogue simple sans commandes supplémentaires spécifiées (ne sera pas mis à l&#39;échelle sur `catalog::maxPix`).

Si d’autres commandes sont spécifiées dans la requête, une zone cliquable composite est renvoyée, dérivée par mise à l’échelle, recadrage, rotation et superposition de toutes les commandes `catalog::Map` et/ou `map=` incluses dans la requête, tout comme les données d’image seraient associées à `req=img`.

Spécifiez `text` ou omettez le second paramètre pour renvoyer les données de zone cliquable sous la forme d’une chaîne d’élément `HTML <AREA>` avec le type MIME de réponse `text/plain`.

Spécifiez `xml` pour formater la réponse au format XML au lieu de HTML. Le codage de texte peut être spécifié facultativement. The default is `UTF-8`.

Renvoie une chaîne vide (ou un élément `<AREA>` vide) si aucune donnée de mappage n’a été trouvée pour les objets de catalogue spécifiés et/ou si aucun élément `<AREA>` ne reste après le recadrage des images.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS en utilisant la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.

Voir [Zones cliquables](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
