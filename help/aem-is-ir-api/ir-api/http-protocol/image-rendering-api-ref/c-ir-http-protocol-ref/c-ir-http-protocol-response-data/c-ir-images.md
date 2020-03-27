---
description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req= ou si req= a l’une des valeurs suivantes img, debug
seo-description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req= ou si req= a l’une des valeurs suivantes img, debug
seo-title: Images
solution: Experience Manager
title: Images
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Images{#images}

Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req= ou si req= possède l’une des valeurs suivantes : img, débogage

Le type MIME de la réponse HTTP est déterminé par `fmt=`, ou, si `fmt=` n’est pas spécifié, dépend de la valeur de `attribute::Format`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l’état &quot;304&quot; (non modifié) et ne renvoyer aucune donnée image en réponse à une `GET` demande conditionnelle (le [!DNL If-Modified-Since] champ étant présent dans le `request-header`).
