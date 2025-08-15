---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 3.7.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1f11a686-7239-4922-a608-5330864184ac
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---

# Opérations : nouvelles et modifiées{#operations-new-and-modified}

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

* Paramètre `name` supprimé.
* Ajout de `excludeFieldArray`.

**getFolders**

* Ajout de `excludeFieldArray`.

**getFolderTree**

* Ajout de `excludeFieldArray` et `getUniqueMetadataValues`.
* `fieldHandle` un paramètre obligatoire.
