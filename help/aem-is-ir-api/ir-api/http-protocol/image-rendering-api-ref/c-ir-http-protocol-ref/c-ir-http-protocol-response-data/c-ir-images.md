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
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# Images{#images}

Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req= ou si req= possède l’une des valeurs suivantes : img, déboguer

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n&#39;est pas spécifié, il dépend de la valeur de `attribute::Format`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l&#39;état &quot;304&quot; (non modifié) et ne pas renvoyer de données d&#39;image en réponse à une demande `GET` conditionnelle (avec le champ [!DNL If-Modified-Since] présent dans `request-header`).
