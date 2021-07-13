---
description: L'image existe.
solution: Experience Manager
title: existe
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 10%

---

# existe{#exists}

L&#39;image existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identifiant de requête unique

Renvoie une propriété unique nommée `catalogRecord.exists`. La valeur de la propriété est définie sur &quot;1&quot; si l’entrée de catalogue spécifiée existe dans l’image ou le catalogue par défaut, sinon elle est définie sur &quot;0&quot;. `req=exists` les requêtes par rapport au  `/is/content` contexte indiquent la présence ou l’absence d’un enregistrement spécifié dans le catalogue de contenu statique.

Les autres commandes de la chaîne de requête sont ignorées. La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `attribute::NonImgExpiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
