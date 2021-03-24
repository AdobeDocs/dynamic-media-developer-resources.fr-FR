---
description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.
solution: Experience Manager
title: Démarrage ou arrêt sous Linux
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Démarrage ou arrêt sous Linux{#starting-or-stopping-on-linux}

Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.

* Le script permettant de début, d’arrêter et de vérifier l’état de la diffusion d’images se trouve dans le dossier [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* Les administrateurs système doivent connaître l’alternative suivante :

   `/sbin/service ImageServing {start|stop|status}`
