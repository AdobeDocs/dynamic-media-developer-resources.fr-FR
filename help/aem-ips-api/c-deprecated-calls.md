---
title: Appels obsolètes
description: Les appels d’API Image Production System et leurs paramètres associés qui ne sont plus utilisés ou pris en charge dans Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: 72f9cd1b1de82cbeeb8d41fb0f1cf0b51744a8a3
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---

# Appels obsolètes{#deprecated-calls}

Les appels d’API Image Production System et leurs paramètres associés qui ne sont plus utilisés.

## Appels obsolètes {#topic-654c0466e6434fe4a95953322255b08c}

Les appels d’API Image Production System et leurs paramètres associés qui ne sont plus utilisés dans Dynamic Media.

* `ExcludeMasterVideoFromAVS` - Obsolète de [Types de données](/help/aem-ips-api/types/c-data-types/c-data-types.md). Ce paramètre a exclu la vidéo Principale de la visionneuse de vidéos adaptative. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre vous permet d’ajouter un événement Media Portal à IPS.
* `getMediaPortalEvent` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre vous permet d’obtenir des événements Media Portal correspondant à des critères spécifiés.
* `getCdnCacheInvalidationStatus` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre est désormais obsolète, car la variable `cdnCacheInvalidation` invalide presque immédiatement le cache (~5 secondes). Par conséquent, l’interrogation de l’état d’invalidation n’est plus nécessaire.
