---
description: Demande de validation.
seo-description: Demande de validation.
seo-title: valider
solution: Experience Manager
title: valider
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---


# valider{#validate}

Demande de validation.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Identificateur de requête unique. </p></td> 
 </tr> 
</table>

Analyse la chaîne de requête comme si `req=img` était spécifié, mais sans substituer de variables ni évaluer les objets référencés (images, profils ICC, polices, etc.). La réponse d’erreur standard est renvoyée en cas d’échec de l’analyse, sinon la propriété suivante est renvoyée :

`request.isValid=1`

La réponse HTTP ne peut pas être mise en cache.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS en utilisant la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
