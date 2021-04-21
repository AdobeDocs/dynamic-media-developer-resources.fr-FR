---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.7.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 1%

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

