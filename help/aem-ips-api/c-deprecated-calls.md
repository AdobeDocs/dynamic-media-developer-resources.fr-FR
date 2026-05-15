---
title: Appels obsolètes
description: Appels d’API du système de production d’images et paramètres associés qui ne sont plus utilisés ni pris en charge dans  [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
autotag-review: '2026-05-13T21:03:57.183Z'
TQID: 'https://experienceleague.adobe.com/JLoyXksHQ-LAXXxfY71Dv-FOE0trpt-RzcKcV-Pv96I'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 0%

---

# Appels obsolètes{#deprecated-calls}

Appels de l’API Image Production System et paramètres associés qui ne sont plus utilisés.

## Appels obsolètes {#topic-654c0466e6434fe4a95953322255b08c}

Appels de l’API Image Production System et paramètres associés qui ne sont plus utilisés dans [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Obsolète de [Types de données](/help/aem-ips-api/types/c-data-types/c-data-types.md). Ce paramètre exclut la vidéo principale de la visionneuse de vidéos adaptative. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre permet d’ajouter un événement Media Portal à IPS.
* `getMediaPortalEvent` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre vous permet d’obtenir des événements de portail multimédia correspondant à des critères spécifiés.
* `getCdnCacheInvalidationStatus` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre est désormais obsolète, car le paramètre `cdnCacheInvalidation` invalide le cache presque immédiatement (~5 secondes). Par conséquent, l’interrogation pour le statut d’invalidation n’est plus nécessaire.
