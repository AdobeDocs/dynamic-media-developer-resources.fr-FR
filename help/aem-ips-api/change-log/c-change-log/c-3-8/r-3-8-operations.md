---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.8.
seo-description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.8.
seo-title: Opérations nouvelles et modifiées
solution: Experience Manager
title: Opérations nouvelles et modifiées
topic: Dynamic Media Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---


# Opérations : Nouveau et modifié{#operations-new-and-modified}

Décrit les méthodes d&#39;opérations nouvelles et modifiées pour l&#39;API IPS version 3.8.

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

* Le paramètre facultatif `publishState` vous permet de rechercher l&#39;état de la ressource `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* Le paramètre facultatif `userHandle` permet de récupérer les journaux de tâches envoyés par un utilisateur spécifique.

