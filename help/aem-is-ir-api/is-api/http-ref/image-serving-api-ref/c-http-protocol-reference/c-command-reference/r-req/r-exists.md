---
description: L'image existe.
seo-description: L'image existe.
seo-title: existe
solution: Experience Manager
title: existe
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 10%

---


# existe{#exists}

L&#39;image existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identifiant de demande unique

Renvoie une propriété unique nommée `catalogRecord.exists`. La valeur de la propriété est définie sur &quot;1&quot; si l’entrée de catalogue spécifiée existe dans l’image ou le catalogue par défaut, sinon elle est définie sur &quot;0&quot;. `req=exists` les requêtes par rapport au  `/is/content` contexte indiquent la présence ou l’absence d’un enregistrement spécifié dans le catalogue de contenu statique.

Les autres commandes de la chaîne de requête sont ignorées. La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `attribute::NonImgExpiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS en utilisant la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
