---
description: Demander la validation.
solution: Experience Manager
title: valider
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 1%

---

# valider{#validate}

Demander la validation.

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant unique de la demande. </p></td> 
 </tr> 
</table>

Analyse la chaîne de requête comme si elle `req=img` avait été spécifiée, mais sans substituer de variables ni évaluer les objets référencés (images, profils ICC, polices, etc.). La réponse d’erreur standard est renvoyée si l’analyse échoue, sinon la propriété suivante est renvoyée :

`request.isValid=1`

La réponse HTTP ne peut pas être mise en cache.

Les demandes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Optionnel. La valeur par défaut est `s7jsonResponse`.
