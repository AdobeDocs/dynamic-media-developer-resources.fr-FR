---
title: Démarrage ou arrêt sous Linux®
description: Il existe deux options pour démarrer ou arrêter la diffusion d’images sous Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
TQID: 'https://experienceleague.adobe.com/i3Ai03O29-qmhMpCRNl7MZkqXjRDnQT1M2sVX-Z3eho'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 64
ht-degree: 0%

---

# Démarrage ou arrêt sous Linux® {#starting-or-stopping-on-linux}

Il existe deux options pour démarrer ou arrêter la diffusion d’images sous Linux®.

* Le script permettant de vérifier le statut de la diffusion d’images ou de démarrer et d’arrêter la diffusion d’images se trouve dans le dossier [!DNL ImageServing/bin] :

  `ImageServing.sh {start|stop|restart|status}`
* L’alternative suivante doit être familière aux administrateurs et administratrices système :

  `/sbin/service ImageServing {start|stop|status}`

