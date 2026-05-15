---
description: Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req=img ou req=tmb.
solution: Experience Manager
title: Images
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: 'https://experienceleague.adobe.com/1tStTbuCLrOG8XrPgOw5qH-VujpHXX8Pt0IWXg9329Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 1%

---

# Images{#images}

Les données d’image sont renvoyées si une requête est terminée avec succès et si la requête n’inclut pas de commande req= ou si req=img ou req=tmb.

Le type MIME de la réponse HTTP est déterminé par `fmt=` ou, si `fmt=` n’est pas spécifié, il est `<image/jpeg>`.

Le statut de la réponse HTTP est « 200 OK » si la méthode de requête était une `GET` ou une `HEAD` inconditionnelle.

Le serveur peut répondre avec l’état « 304 » (non modifié) et ne renvoyer aucune donnée d’image en réponse à une demande de `GET` conditionnelle (qui inclut un en-tête `If-Modified-Since` ou `If-None-Match` valide).
