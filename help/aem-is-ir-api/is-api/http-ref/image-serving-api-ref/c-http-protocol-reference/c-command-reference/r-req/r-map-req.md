---
title: carte
description: Données de zone cliquable.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# carte{#map}

Données de zone cliquable.

`req=map[,text|{xml[, *`reqId de`*]}|{json[&id= *`codage`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codage</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | Norme ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant unique de la demande. </p></td> 
 </tr> 
</table>

Renvoie `catalog::Map` sans modification lors de l’interrogation d’une entrée de catalogue simple sans aucune commande supplémentaire spécifiée (ne s’applique pas à `catalog::maxPix`).

Si d’autres commandes sont spécifiées dans la requête, une zone cliquable composite est renvoyée. La zone cliquable composite est dérivée par mise à l’échelle, recadrage, rotation et superposition de toutes les `catalog::Map` commandes et/ou `map=` commandes incluses dans la requête, tout comme les données image le seraient avec `req=img`.

Spécifiez `text` ou omettez le deuxième paramètre afin de pouvoir renvoyer les données de la zone cliquable sous la forme d’une `HTML <AREA>` chaîne d’élément avec réponse de type `text/plain`MIME .

Spécifiez `xml` cette condition afin de pouvoir formater la réponse au format XML plutôt que HTML. Le codage de texte peut être spécifié en option. La valeur par défaut est `UTF-8`.

Renvoie une chaîne vide (ou un élément vide `<AREA>` ) si aucune donnée de carte n’a été trouvée pour les objets de catalogue spécifiés et/ou s’il ne reste aucun `<AREA>` élément après le recadrage des images.

La réponse HTTP peut être mise en cache avec la durée de vie basée sur la base de `catalog::Expiration`.

Les demandes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

Il `<reqHandler>` s’agit du nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Optionnel. La valeur par défaut est `s7jsonResponse`.

Voir [Zones cliquables](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
