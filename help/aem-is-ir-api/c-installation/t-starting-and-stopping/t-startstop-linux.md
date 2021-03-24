---
description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.
solution: Experience Manager
title: Démarrage ou arrêt sous Linux
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
