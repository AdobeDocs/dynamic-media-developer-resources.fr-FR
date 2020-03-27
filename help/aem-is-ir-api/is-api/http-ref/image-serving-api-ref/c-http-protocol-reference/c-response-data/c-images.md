---
description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.
seo-description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.
seo-title: Images
solution: Experience Manager
title: Images
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Images{#images}

Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.

Le type MIME de la réponse HTTP est déterminé par `fmt=`, ou, si `fmt=` n’est pas spécifié, il l’est `<image/jpeg>`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l’état &quot;304&quot; (non modifié) et ne renvoyer aucune donnée image en réponse à une `GET` demande conditionnelle (qui inclut un `If-Modified-Since` `If-None-Match` en-tête ou un en-tête valide).
