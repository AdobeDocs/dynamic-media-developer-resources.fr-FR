---
description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.
seo-description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.
seo-title: Démarrage ou arrêt sous Linux
solution: Experience Manager
title: Démarrage ou arrêt sous Linux
topic: Scene7 Image Serving - Image Rendering API
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# Démarrage ou arrêt sous Linux{#starting-or-stopping-on-linux}

Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.

* Le script permettant de début, d’arrêter et de vérifier l’état de la diffusion d’images se trouve dans le dossier [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* Les administrateurs système doivent connaître l’alternative suivante :

   `/sbin/service ImageServing {start|stop|status}`
