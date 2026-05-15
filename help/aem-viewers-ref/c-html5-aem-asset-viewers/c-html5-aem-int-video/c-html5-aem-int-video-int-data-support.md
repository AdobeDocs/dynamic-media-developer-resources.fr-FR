---
title: Prise en charge des données interactives
description: La visionneuse de vidéos interactives prend en charge le rendu d’échantillons interactifs en fonction des données interactives transmises à la visionneuse en tant que paramètre de configuration.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
TQID: 'https://experienceleague.adobe.com/HE4LeluT9FWi8xgQf259b1yakK0oQjeR3rDME0juZiU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 0%

---

# Prise en charge des données interactives{#interactive-data-support}

La visionneuse de vidéos interactives prend en charge le rendu d’échantillons interactifs en fonction des données interactives transmises à la visionneuse en tant que paramètre de configuration.

L’échantillon actuellement visible correspond à la région temporelle de la vidéo à laquelle il est associé. Cliquez ou appuyez sur l’échantillon interactif pour déclencher l’action qui lui est attribuée au moment de la création.

L’échantillon interactif peut activer un aperçu rapide sur la page web d’hébergement en déclenchant un rappel JavaScript ou rediriger l’utilisateur vers une page web externe.

## À propos de l’aperçu rapide {#section-7990e44f641042d2a38ba20c9413b3f8}

Ces types d’échantillons interactifs doivent être créés à l’aide du type d’action « aperçu rapide » dans Adobe Experience Manager Assets - À la demande. Lorsqu’un utilisateur active cet échantillon, la visionneuse exécute `quickViewActivate` rappel JavaScript et lui transmet les données d’échantillon. Il est prévu que la page web d’incorporation écoute ce rappel et, lorsqu’elle se déclenche, la page ouvre sa propre mise en œuvre d’aperçu rapide.

## Rediriger vers une page web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

Les échantillons créés pour le type d’action « aperçu rapide » dans Experience Manager Assets redirigent l’utilisateur à la demande vers une URL externe. Selon les paramètres au moment de la création, l’URL peut s’ouvrir dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
