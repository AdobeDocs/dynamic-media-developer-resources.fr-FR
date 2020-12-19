---
description: La visionneuse de vidéos interactive prend en charge le rendu des échantillons interactifs en fonction des données interactives transmises à la visionneuse en tant que paramètre de configuration.
seo-description: La visionneuse de vidéos interactive prend en charge le rendu des échantillons interactifs en fonction des données interactives transmises à la visionneuse en tant que paramètre de configuration.
seo-title: Prise en charge des données interactives
solution: Experience Manager
title: Prise en charge des données interactives
topic: Dynamic media
uuid: 70b2ec2e-0ea7-461d-a185-731fb0ef8f3e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Prise en charge des données interactives{#interactive-data-support}

La visionneuse de vidéos interactive prend en charge le rendu des échantillons interactifs en fonction des données interactives transmises à la visionneuse en tant que paramètre de configuration.

L’échantillon actuellement visible correspond à la région de temps de la vidéo à laquelle il est associé. Un clic ou un appui sur l’échantillon interactif déclenche l’action qui lui est affectée au moment de la création.

L’échantillon interactif peut soit activer une Vue rapide sur la page Web d’hébergement en déclenchant un rappel JavaScript, soit rediriger l’utilisateur vers une page Web externe.

## A propos de la Vue rapide {#section-7990e44f641042d2a38ba20c9413b3f8}

Ces types de nuances interactives doivent être créés à l’aide du type d’action &quot;quickview&quot; en AEM Assets - on-demand. Lorsqu’un utilisateur active une telle nuance, le lecteur exécute le rappel JavaScript `quickViewActivate` et lui transmet les données d’échantillon. Il est prévu que la page Web incorporée écoute ce rappel et, lorsqu’elle se déclenche, la page ouvre sa propre mise en oeuvre de Vue rapide.

## Redirection vers une page Web externe {#section-32ebe3c3a7f74892a428c5d48801de4d}

Echantillons créés pour le type d’action &quot;quickview&quot; en AEM Assets : redirigez l’utilisateur à la demande vers une URL externe. Selon les paramètres définis au moment de la création, l’URL peut s’ouvrir soit dans un nouvel onglet de navigateur, soit dans la même fenêtre, soit dans la fenêtre de navigateur nommée.
