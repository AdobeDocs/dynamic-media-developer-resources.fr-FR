---
description: Données de visionneuse d’images issues du catalogue d’images. Renvoie les données de visionneuse d’images pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# imageset{#imageset}

Données de visionneuse d’images issues du catalogue d’images. Renvoie les données de visionneuse d’images pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.

`req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> encoding</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Le contenu de `catalog::ImageSet` est renvoyé sans autre modification (à l’exception de la localisation de chaîne, le cas échéant), suivi d’un terminateur d’une seule ligne (CR/LF). Si le chemin d’URL ne se résout pas en une entrée de catalogue valide, la réponse se compose uniquement d’un terminateur d’une seule ligne.

Les autres commandes de la chaîne de requête sont ignorées. La réponse HTTP peut être mise en cache avec le TTL basé sur `catalog::NonImgExpiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
