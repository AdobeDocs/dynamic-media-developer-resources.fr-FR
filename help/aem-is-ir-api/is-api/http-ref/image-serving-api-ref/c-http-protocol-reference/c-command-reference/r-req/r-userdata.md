---
description: Données utilisateur du catalogue d’images. Renvoie les données utilisateur pour l’entrée de catalogue d’images spécifiée dans le chemin d’accès à l’URL.
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 6%

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

Le contenu de `catalog::UserData` est renvoyé. Lorsque le format &quot;texte&quot; est spécifié, toutes les instances de `??` dans `catalog::UserData`sont remplacées par des terminateurs de ligne et un terminateur de ligne unique (CR/LF) est ajouté à la fin. Si le chemin d’accès à l’URL ne se résout pas à une entrée de catalogue valide, la réponse se compose uniquement d’un terminateur de ligne unique. Une mise en forme appropriée est appliquée lorsque le format &quot;xml&quot; ou &quot;json&quot; est demandé.

Les autres commandes de la chaîne de requête sont ignorées.

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `catalog::Expiration`.

>[!NOTE]
>
>Le caractère deux-points n&#39;est pas autorisé dans les noms de clés de propriété userdata.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS en utilisant la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
