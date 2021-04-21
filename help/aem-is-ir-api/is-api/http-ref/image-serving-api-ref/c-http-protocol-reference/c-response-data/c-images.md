---
description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.
solution: Experience Manager
title: Images
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 1%

---


# Images{#images}

Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n&#39;est pas spécifié, il est `<image/jpeg>`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l&#39;état &quot;304&quot; (non modifié) et ne pas renvoyer de données d&#39;image en réponse à une demande conditionnelle `GET` (qui inclut un en-tête `If-Modified-Since` ou `If-None-Match` valide).
