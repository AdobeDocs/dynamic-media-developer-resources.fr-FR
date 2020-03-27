---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.8.
seo-description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.8.
seo-title: Opérations nouvelles et modifiées
solution: Experience Manager
title: Opérations nouvelles et modifiées
topic: Scene7 Image Production System API
uuid: e836c5af-53b8-4bfa-a93a-98750cca9745
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

* Le `publishState` paramètre facultatif vous permet de rechercher l’état `MarkedForPublish/NotMarkedForPublish` du fichier.

**getJobLogs**

* Le `userHandle` paramètre facultatif vous permet de récupérer les journaux de tâches envoyés par un utilisateur spécifique.

