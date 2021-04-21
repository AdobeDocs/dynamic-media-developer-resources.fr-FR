---
description: Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req= ou si req= possède l’une des valeurs suivantes img, debug.
solution: Experience Manager
title: Images
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 1%

---


# Images{#images}

Les données image sont renvoyées si une requête aboutit et si la requête n’inclut pas de commande req= ou si req= possède l’une des valeurs suivantes : img, déboguer

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n&#39;est pas spécifié, il dépend de la valeur de `attribute::Format`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l&#39;état &quot;304&quot; (non modifié) et ne pas renvoyer de données d&#39;image en réponse à une demande `GET` conditionnelle (avec le champ [!DNL If-Modified-Since] présent dans `request-header`).
