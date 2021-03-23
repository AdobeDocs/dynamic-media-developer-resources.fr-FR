---
description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.
seo-description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.
seo-title: Démarrage ou arrêt sous Linux
solution: Experience Manager
title: Démarrage ou arrêt sous Linux
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# Démarrage ou arrêt sous Linux{#starting-or-stopping-on-linux}

Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.

* Le script permettant de début, d’arrêter et de vérifier l’état de la diffusion d’images se trouve dans le dossier [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* Les administrateurs système doivent connaître l’alternative suivante :

   `/sbin/service ImageServing {start|stop|status}`
