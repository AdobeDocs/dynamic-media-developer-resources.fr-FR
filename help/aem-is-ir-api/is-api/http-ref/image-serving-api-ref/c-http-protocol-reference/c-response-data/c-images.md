---
description: Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req=img ou req=tmb.
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

Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req=img ou req=tmb.

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n’est pas spécifié, il est `<image/jpeg>`.

Le statut de la réponse HTTP est « 200 OK » si la méthode de requête était une `GET` ou une `HEAD` inconditionnelle.

Le serveur peut répondre avec l’état « 304 » (non modifié) et ne renvoyer aucune donnée d’image en réponse à une demande de `GET` conditionnelle (qui inclut un en-tête `If-Modified-Since` ou `If-None-Match` valide).
