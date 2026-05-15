---
description: Données de visionneuse d’images provenant du catalogue d’images. Renvoie les données de visionneuse d’images pour l’entrée de catalogue d’images spécifiée dans le chemin URL.
solution: Experience Manager
title: visionneuse d’images
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
TQID: 'https://experienceleague.adobe.com/1PbZjs--lk7GcyXU1F-AJ-vWcgwVX9JFivvbnTGrWKQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# visionneuse d’images{#imageset}

Données de visionneuse d’images provenant du catalogue d’images. Renvoie les données de visionneuse d’images pour l’entrée de catalogue d’images spécifiée dans le chemin URL.

`req=imageset[,text|javascript|{xml[, *`encoding`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Encodage de </span></span> <span class="codeph"><span class="varname"></p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

Le contenu de `catalog::ImageSet` est renvoyé sans autre modification (à l’exception de la localisation de chaîne, le cas échéant), suivi d’une terminaison d’une seule ligne (CR/LF). Si le chemin d’URL ne correspond pas à une entrée de catalogue valide, la réponse se compose uniquement d’une terminaison d’une seule ligne.

Les autres commandes de la chaîne de requête sont ignorées. La réponse HTTP peut être mise en cache avec la TTL basée sur `catalog::NonImgExpiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
