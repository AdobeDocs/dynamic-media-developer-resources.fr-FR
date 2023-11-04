---
description: Données utilisateur du catalogue d’images. Renvoie les données utilisateur pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 7%

---

# userdata{#userdata}

Données utilisateur du catalogue d’images. Renvoie les données utilisateur pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.

`req=userdata[,text|{xml[, *`encodage`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> encodage</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

Le contenu de `catalog::UserData` sont renvoyées. Lorsque le format &quot;texte&quot; est spécifié, toutes les instances de `??` in `catalog::UserData`sont remplacés par des terminateurs de ligne, et un terminateur d’une seule ligne (CR/LF) est ajouté à la fin. Si le chemin d’URL ne se résout pas en une entrée de catalogue valide, la réponse se compose uniquement d’un terminateur d’une seule ligne. La mise en forme appropriée est appliquée lorsque le format &quot;xml&quot; ou &quot;json&quot; est demandé.

Les autres commandes de la chaîne de requête sont ignorées.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

>[!NOTE]
>
>Le caractère deux-points n’est pas autorisé dans les noms de clés de propriété userdata .

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue de `req=` parameter:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Par défaut : `s7jsonResponse`.
