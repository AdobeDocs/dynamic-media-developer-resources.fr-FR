---
description: Données de visionneuse d’images du catalogue d’images. Renvoie les données de visionneuse d’images pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.
seo-description: Données de visionneuse d’images du catalogue d’images. Renvoie les données de visionneuse d’images pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.
seo-title: imageset
solution: Experience Manager
title: imageset
topic: Scene7 Image Serving - Image Rendering API
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageset{#imageset}

Données de visionneuse d’images du catalogue d’images. Renvoie les données de visionneuse d’images pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encodage</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Le contenu de `catalog::ImageSet` est renvoyé sans modification supplémentaire (sauf les  de chaîne, le cas échéant), suivi d’un terminateur de ligne unique (CR/LF). Si le chemin d’accès à l’URL ne se résout pas à une entrée de catalogue valide, la réponse se compose uniquement d’un terminateur de ligne unique.

Les autres commandes de la chaîne de requête sont ignorées. La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::NonImgExpiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Default is `s7jsonResponse`.
