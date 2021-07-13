---
description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.
solution: Experience Manager
title: Démarrage ou arrêt sous Linux
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Démarrage ou arrêt sous Linux{#starting-or-stopping-on-linux}

Il existe deux options pour démarrer ou arrêter Image Serving sous Linux.

* Le script permettant de démarrer, arrêter et vérifier l’état du serveur d’images se trouve dans le dossier [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* L’alternative suivante doit être familière aux administrateurs système :

   `/sbin/service ImageServing {start|stop|status}`
