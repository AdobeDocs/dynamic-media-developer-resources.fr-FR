---
title: Images
description: Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req= a l’une des valeurs suivantes img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 1%

---

# Images{#images}

Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req= a l’une des valeurs suivantes : img, debug

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n’est pas spécifié, il dépend de la valeur de `attribute::Format`.

Le statut de la réponse HTTP est « 200 OK » si la méthode de requête était une `GET` ou une `HEAD` inconditionnelle.

Le serveur peut répondre avec le statut &#39;304&#39; (non modifié) et ne pas renvoyer de données d’image en réponse à une demande de `GET` conditionnelle (avec le champ [!DNL If-Modified-Since] présent dans le `request-header`).
