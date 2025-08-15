---
title: Images
description: Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req= a l’une des valeurs suivantes img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 1%

---

# Images{#images}

Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req= a l’une des valeurs suivantes : img, debug

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n’est pas spécifié, il dépend de la valeur de `attribute::Format`.

Le statut de la réponse HTTP est « 200 OK » si la méthode de requête était une `GET` ou une `HEAD` inconditionnelle.

Le serveur peut répondre avec le statut &#39;304&#39; (non modifié) et ne pas renvoyer de données d’image en réponse à une demande de `GET` conditionnelle (avec le champ [!DNL If-Modified-Since] présent dans le `request-header`).
