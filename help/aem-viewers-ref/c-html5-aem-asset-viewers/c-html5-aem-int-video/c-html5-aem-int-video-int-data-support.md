---
title: Prise en charge des données interactives
description: La visionneuse de vidéo interactive prend en charge le rendu d’échantillons interactifs en fonction des données interactives transmises à la visionneuse en tant que paramètre de configuration.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Prise en charge des données interactives{#interactive-data-support}

La visionneuse de vidéo interactive prend en charge le rendu d’échantillons interactifs en fonction des données interactives transmises à la visionneuse en tant que paramètre de configuration.

L’échantillon actuellement visible correspond à la région temporelle de la vidéo à laquelle il est associé. Cliquez ou appuyez sur l’échantillon interactif pour déclencher l’action qui lui est affectée au moment de la création.

L’échantillon interactif peut activer un aperçu rapide sur la page web d’hébergement en déclenchant un rappel JavaScript ou rediriger l’utilisateur vers une page web externe.

## Aperçu rapide {#section-7990e44f641042d2a38ba20c9413b3f8}

Ces types d’échantillons interactifs doivent être créés à l’aide du type d’action &quot;quickview&quot; dans Adobe Experience Manager Assets - On-demand. Lorsqu’un utilisateur active un tel échantillon, la visionneuse exécute le rappel JavaScript `quickViewActivate` et lui transmet les données d’échantillon. Il est prévu que la page web d’intégration écoute ce rappel et, lorsqu’elle se déclenche, la page ouvre sa propre mise en oeuvre d’aperçu rapide.

## Redirection vers une page web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

Nuancier créé pour le type d’action &quot;quickview&quot; dans Experience Manager Assets : redirigez l’utilisateur vers une URL externe. Selon les paramètres définis au moment de la création, l’URL peut s’ouvrir dans un nouvel onglet du navigateur, dans la même fenêtre ou dans la fenêtre du navigateur nommé.
