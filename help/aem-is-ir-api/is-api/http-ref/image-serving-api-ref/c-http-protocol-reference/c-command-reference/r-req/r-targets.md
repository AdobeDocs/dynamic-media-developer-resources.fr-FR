---
description: Données de cibles de zoom du catalogue d’images. Renvoie les données de cible de zoom pour l’entrée de catalogue d’images spécifiée dans le chemin d’URL.
solution: Experience Manager
title: cibles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 1%

---

# cibles{#targets}

Données de cibles de zoom du catalogue d’images. Renvoie les données de cible de zoom pour l’entrée de catalogue d’images spécifiée dans le chemin d’URL.

`req=targets[,text|{xml[, *`reqId de`*]}|{json[&id= *`codage`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codage</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | Norme ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant unique de la demande. </p></td> 
 </tr> 
</table>

Le contenu de `catalog::Targets` est renvoyé. Lorsque le format &#39;texte&#39; est demandé, toutes les instances de in `??` sont remplacées par des terminateurs de `catalog::Targets` ligne, et un terminateur d’une seule ligne ( `CR/LF`) est ajouté à la fin. Si le chemin d’accès à l’URL ne renvoie pas à une entrée de catalogue valide, la réponse consiste uniquement en un terminateur d’une seule ligne. Une mise en forme appropriée est appliquée lorsque le format &#39;xml&#39; ou &#39;json&#39; est demandé.

Les autres commandes de la chaîne de requête sont ignorées.

La réponse HTTP peut être mise en cache avec la durée de vie basée sur la base de `catalog::Expiration`.

Les demandes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Optionnel. La valeur par défaut est `s7jsonResponse`.
