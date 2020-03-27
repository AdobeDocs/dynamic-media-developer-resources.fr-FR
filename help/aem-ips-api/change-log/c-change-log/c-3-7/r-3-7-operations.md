---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.7.
seo-description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.7.
seo-title: Opérations nouvelles et modifiées
solution: Experience Manager
title: Opérations nouvelles et modifiées
topic: Scene7 Image Production System API
uuid: 3c163157-cd0d-4887-a1f0-7941d96c36f9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Opérations : Nouveau et modifié{#operations-new-and-modified}

Décrit les méthodes d&#39;opérations nouvelles et modifiées pour l&#39;API IPS version 3.7.

Syntaxe

## Nouvelles opérations {#section-c4d34a58f8194d548fbe26ab3764ea58}

* `moveAsset`
* `renameAsset`
* `deleteAsset`
* `createFolder`
* `deleteFolder`
* `getActiveJobs`
* `getScheduledJobs`
* `getJobLogs`
* `getJbLogDetails`
* `submitJob`
* `stopJob`
* `pauseJob`
* `resumeJob`
* `executeJob`
* `deleteJob`

## Opérations modifiées {#section-596ea55a371e4c2ab5531e21ea9d8090}

**searchAsset**

* Suppression `name` du paramètre.
* Added `excludeFieldArray`.

**getFolders**

* Added `excludeFieldArray`.

**getFolderTree**

* Ajout `excludeFieldArray` et `getUniqueMetadataValues`.
* Ajout `fieldHandle` d’un paramètre obligatoire.

