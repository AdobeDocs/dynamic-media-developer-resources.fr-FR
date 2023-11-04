---
description: Zoom cible les données du catalogue d’images. Renvoie les données de la cible de zoom pour l’entrée du catalogue d’images spécifiée dans le chemin d’accès à l’URL.
solution: Experience Manager
title: cibles
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 7%

---

# cibles{#targets}

Zoom cible les données du catalogue d’images. Renvoie les données de la cible de zoom pour l’entrée du catalogue d’images spécifiée dans le chemin d’accès à l’URL.

`req=targets[,text|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Le contenu de `catalog::Targets` sont renvoyées. Lorsque le format &quot;texte&quot; est demandé, toutes les instances de `??` in `catalog::Targets` sont remplacés par des terminateurs de ligne et un terminateur d’une seule ligne ( `CR/LF`) est ajouté à la fin. Si le chemin d’URL ne se résout pas en une entrée de catalogue valide, la réponse se compose uniquement d’un terminateur d’une seule ligne. La mise en forme appropriée est appliquée lorsque le format &quot;xml&quot; ou &quot;json&quot; est demandé.

Les autres commandes de la chaîne de requête sont ignorées.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue de `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Par défaut : `s7jsonResponse`.
