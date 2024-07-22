---
description: Les données image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.
solution: Experience Manager
title: Images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 1%

---

# Images{#images}

Les données image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req=, ou si req=img ou req=tmb.

Le type MIME de réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n’est pas spécifié, il s’agit de `<image/jpeg>`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l’état &quot;304&quot; (non modifié) et ne renvoyer aucune donnée d’image en réponse à une demande `GET` conditionnelle (qui inclut un en-tête `If-Modified-Since` ou `If-None-Match` valide).
