---
description: L’image existe.
solution: Experience Manager
title: existe
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
TQID: 'https://experienceleague.adobe.com/JyGNYH5-vW7FbZbMcMk2mQFB7rrrzYd0FpvsBbI-Zi4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 2%

---

# existe{#exists}

L’image existe.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

Identifiant de requête unique *`reqId`*

Renvoie une seule propriété nommée `catalogRecord.exists`. La valeur de la propriété est définie sur « 1 » si l’entrée de catalogue spécifiée existe dans l’image ou le catalogue par défaut, sinon elle est définie sur « 0 ». `req=exists` requêtes effectuées dans le contexte `/is/content` indiquent la présence ou l’absence d’un enregistrement spécifié dans le catalogue de contenu statique.

Les autres commandes de la chaîne de requête sont ignorées. La réponse HTTP peut être mise en cache avec la TTL basée sur `attribute::NonImgExpiration`.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.
