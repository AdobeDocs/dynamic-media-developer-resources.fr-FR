---
title: Appels obsolètes
description: Les appels d’API Image Production System et leurs paramètres associés qui ne sont plus utilisés ou pris en charge dans  [!DNL Dynamic Media].
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f6711780-9a96-4a61-9066-8d83316758c3
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# Appels obsolètes{#deprecated-calls}

Les appels d’API Image Production System et leurs paramètres associés qui ne sont plus utilisés.

## Appels obsolètes {#topic-654c0466e6434fe4a95953322255b08c}

Les appels d’API Image Production System et leurs paramètres associés qui ne sont plus utilisés dans [!DNL Dynamic Media].

* `ExcludeMasterVideoFromAVS` - Obsolète de [Types de données](/help/aem-ips-api/types/c-data-types/c-data-types.md). Ce paramètre a exclu la vidéo principale de la visionneuse de vidéos adaptative. <!-- Adobe is ending support for this parameter on September 1, 2022. -->
* `addMediaPortalEvent` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre vous permet d’ajouter un événement Media Portal à IPS.
* `getMediaPortalEvent` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre vous permet d’obtenir des événements Media Portal correspondant à des critères spécifiés.
* `getCdnCacheInvalidationStatus` - Obsolète de [Opérations](/help/aem-ips-api/operations/c-operations-intro/c-operations-intro.md). Ce paramètre est désormais obsolète car le paramètre `cdnCacheInvalidation` invalide le cache presque immédiatement (~5 secondes). Par conséquent, l’interrogation de l’état d’invalidation n’est plus nécessaire.
