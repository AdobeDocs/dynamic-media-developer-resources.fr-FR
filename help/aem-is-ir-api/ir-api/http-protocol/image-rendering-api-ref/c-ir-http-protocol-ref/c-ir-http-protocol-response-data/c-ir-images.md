---
description: Les données image sont renvoyées si une requête se termine correctement et si la requête n’inclut pas de commande req= ou si req= a l’une des valeurs suivantes img, déboguez.
solution: Experience Manager
title: Images
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 1%

---

# Images{#images}

Les données image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req= possède l’une des valeurs suivantes : img, déboguer

Le type MIME de réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n’est pas spécifié, il dépend de la valeur de `attribute::Format`.

L’état de la réponse HTTP est &quot;200 OK&quot; si la méthode de requête était inconditionnelle `GET` ou `HEAD`.

Le serveur peut répondre avec l’état &quot;304&quot; (non modifié) et ne pas renvoyer de données image en réponse à une demande `GET` conditionnelle (avec le champ [!DNL If-Modified-Since] présent dans la balise `request-header`).
