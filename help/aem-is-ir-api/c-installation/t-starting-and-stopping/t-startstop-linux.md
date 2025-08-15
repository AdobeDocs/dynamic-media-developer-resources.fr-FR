---
title: Démarrage ou arrêt sous Linux®
description: Il existe deux options pour démarrer ou arrêter la diffusion d’images sous Linux®.
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

Il existe deux options pour démarrer ou arrêter la diffusion d’images sous Linux®.

* Le script permettant de vérifier l’état de la fonction Serveur d’images, ou de démarrer et d’arrêter la Diffusion d’images, se trouve dans le [!DNL ImageServing/bin] dossier suivant :

  `ImageServing.sh {start|stop|restart|status}`
* L’alternative suivante doit être familière aux administrateurs système :

  `/sbin/service ImageServing {start|stop|status}`
