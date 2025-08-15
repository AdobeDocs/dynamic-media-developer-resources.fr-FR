---
title: Prise en charge des données interactives
description: La visionneuse de vidéos interactives prend en charge le rendu d’échantillons interactifs basés sur les données interactives transmises à la visionneuse en tant que paramètre de configuration.
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

La visionneuse de vidéos interactives prend en charge le rendu d’échantillons interactifs basés sur les données interactives transmises à la visionneuse en tant que paramètre de configuration.

La nuance actuellement visible correspond à la région temporelle de la vidéo à laquelle elle est associée. Le fait de cliquer ou d’appuyer sur l’échantillon interactif déclenche l’action qui lui est affectée au moment de l’auteur.

L’échantillon interactif peut activer un aperçu rapide sur la page Web d’hébergement en déclenchant un rappel JavaScript ou rediriger l’utilisateur vers une page Web externe.

## À propos de l’aperçu rapide {#section-7990e44f641042d2a38ba20c9413b3f8}

Ces types d’échantillons interactifs doivent être créés à l’aide du type d’action « aperçu rapide » dans Adobe Experience Manager Assets - À la demande. Lorsqu’un utilisateur active un tel échantillon, il exécute `quickViewActivate` JavaScript rappel et lui transmet les données de l’échantillon. Il est prévu que la page Web d’incorporation écoute ce rappel et, lorsqu’il se déclenche, la page ouvre sa propre implémentation d’aperçu rapide.

## Redirection vers une page Web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

Les échantillons créés pour le type d’action « aperçu rapide » dans Experience Manager Assets - on-demand redirigent l’utilisateur vers une URL externe. Selon les paramètres au moment de la création, l’URL peut s’ouvrir soit dans un nouvel onglet de navigateur, dans la même fenêtre ou dans la fenêtre de navigateur nommée.
