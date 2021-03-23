---
description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.
seo-description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.
seo-title: Images
solution: Experience Manager
title: Images
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---


# Images{#images}

Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n&#39;est pas spécifié, il est `<image/jpeg>`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l&#39;état &quot;304&quot; (non modifié) et ne pas renvoyer de données d&#39;image en réponse à une demande conditionnelle `GET` (qui inclut un en-tête `If-Modified-Since` ou `If-None-Match` valide).
