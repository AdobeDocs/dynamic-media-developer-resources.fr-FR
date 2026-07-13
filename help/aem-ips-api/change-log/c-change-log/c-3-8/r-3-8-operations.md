---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.8.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8f4fe698-afe8-4ce6-904d-42fa67dee4dd
TQID: 'https://experienceleague.adobe.com/ABGdwOL99oGAXt9UBLNVYQrGxAQ3S9nlDDTHRZNt1Xo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 62
ht-degree: 1%

---

# Opérations : nouvelles et modifiées{#operations-new-and-modified}

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

* Le paramètre de `publishState` facultatif vous permet d’effectuer une recherche sur l’état de la ressource `MarkedForPublish/NotMarkedForPublish`.

**getJobLogs**

* Le paramètre `userHandle` facultatif permet de récupérer les logs de traitement envoyés par un utilisateur spécifique.

