---
description: Zoom cible les données du catalogue d’images. Renvoie les données de cible de zoom pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès de l’URL.
seo-description: Zoom cible les données du catalogue d’images. Renvoie les données de cible de zoom pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès de l’URL.
seo-title: cibles
solution: Experience Manager
title: cibles
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 6%

---


# cibles{#targets}

Zoom cible les données du catalogue d’images. Renvoie les données de cible de zoom pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès de l’URL.

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encodage</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>Identificateur de requête unique. </p></td> 
 </tr> 
</table>

Le contenu de `catalog::Targets` est renvoyé. Lorsque le format &quot;texte&quot; est demandé, toutes les instances de `??` dans `catalog::Targets` sont remplacées par des terminateurs de ligne et un terminateur de ligne unique ( `CR/LF`) est ajouté à la fin. Si le chemin d’accès à l’URL ne se résout pas à une entrée de catalogue valide, la réponse se compose uniquement d’un terminateur de ligne unique. Une mise en forme appropriée est appliquée lorsque le format &quot;xml&quot; ou &quot;json&quot; est demandé.

Les autres commandes de la chaîne de requête sont ignorées.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS en utilisant la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
