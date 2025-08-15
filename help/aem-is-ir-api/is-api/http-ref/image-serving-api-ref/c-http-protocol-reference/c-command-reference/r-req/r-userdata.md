---
description: Données utilisateur provenant du catalogue d’images. Renvoie les données utilisateur pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.
solution: Experience Manager
title: Données utilisateur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# Données utilisateur{#userdata}

Données utilisateur provenant du catalogue d’images. Renvoie les données utilisateur pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.

`req=userdata[,text|{xml[, *`codage`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codage</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | Norme ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Le contenu de `catalog::UserData` est renvoyé. Lorsque le format &#39;texte&#39; est spécifié, toutes les instances de in `??`sont remplacées par des terminateurs de `catalog::UserData` ligne, et un terminateur d’une seule ligne (CR/LF) est ajouté à la fin. Si le chemin d’accès à l’URL ne renvoie pas à une entrée de catalogue valide, la réponse consiste uniquement en un terminateur d’une seule ligne. Une mise en forme appropriée est appliquée lorsque le format &#39;xml&#39; ou &#39;json&#39; est demandé.

Les autres commandes de la chaîne de requête sont ignorées.

La réponse HTTP peut être mise en cache avec la durée de vie basée sur la base de `catalog::Expiration`.

>[!NOTE]
>
>Le caractère deux-points n’est pas autorisé dans les noms de clés de propriété userdata.

Les demandes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Optionnel. La valeur par défaut est `s7jsonResponse`.
