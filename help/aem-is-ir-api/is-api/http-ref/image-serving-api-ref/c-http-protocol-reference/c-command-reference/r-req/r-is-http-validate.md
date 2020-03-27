---
description: Demande de validation.
seo-description: Demande de validation.
seo-title: valider
solution: Experience Manager
title: valider
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# valider{#validate}

Demande de validation.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Analyse la chaîne de requête comme si elle `req=img` était spécifiée, mais sans substituer de variables ni évaluer les objets référencés (images, ICC, polices, etc.). La réponse d’erreur standard est renvoyée en cas d’échec de l’analyse ; dans le cas contraire, la propriété suivante est renvoyée :

`request.isValid=1`

La réponse HTTP ne peut pas être mise en cache.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Default is `s7jsonResponse`.
