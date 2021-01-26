---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.7.
solution: Experience Manager
title: Opérations nouvelles et modifiées
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 2%

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

* Suppression du paramètre `name`.
* Ajouté `excludeFieldArray`.

**getFolders**

* Ajouté `excludeFieldArray`.

**getFolderTree**

* Ajouté `excludeFieldArray` et `getUniqueMetadataValues`.
* Ajout de `fieldHandle` paramètre obligatoire.

