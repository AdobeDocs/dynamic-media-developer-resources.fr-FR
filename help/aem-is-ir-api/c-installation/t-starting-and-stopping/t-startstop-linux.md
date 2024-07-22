---
title: Démarrage ou arrêt sous Linux®
description: Il existe deux options pour démarrer ou arrêter Image Serving sous Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Démarrage ou arrêt sous Linux® {#starting-or-stopping-on-linux}

Il existe deux options pour démarrer ou arrêter Image Serving sous Linux®.

* Le script permettant de vérifier l’état du serveur d’images, ou de démarrer et arrêter le serveur d’images, se trouve dans le dossier [!DNL ImageServing/bin] :

  `ImageServing.sh {start|stop|restart|status}`
* L’alternative suivante doit être familière aux administrateurs système :

  `/sbin/service ImageServing {start|stop|status}`
