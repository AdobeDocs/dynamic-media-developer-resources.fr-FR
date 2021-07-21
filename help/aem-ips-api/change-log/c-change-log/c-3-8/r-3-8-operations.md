---
description: Décrit les nouvelles méthodes d’exploitation et les méthodes modifiées pour l’API IPS version 3.8.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 1%

---

# Opérations : Nouveautés et modifications{#operations-new-and-modified}

Décrit les nouvelles méthodes d’exploitation et les méthodes modifiées pour l’API IPS version 3.8.

Syntaxe

## Nouvelles opérations {#section-64f0e4cd01154bb68c4e3e2dd8732ef5}

* `setAssetPublishState`
* `saveZoomTarget`
* `deleteZoomTarget`
* `saveImageMap`
* `deleteImageMap`
* `createImageSet`
* `getImageSetMembers`

## Opérations modifiées {#section-25eee732b69c49d0a27b1f3290f8654a}

**searchAssets**

* Le paramètre facultatif `publishState` vous permet de rechercher l’état de la ressource `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* Le paramètre facultatif `userHandle` vous permet de récupérer les logs de tâches envoyés par un utilisateur spécifique.
