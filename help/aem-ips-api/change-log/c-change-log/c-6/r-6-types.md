---
description: Décrit les types nouveaux et modifiés pour l’API IPS version 6.
solution: Experience Manager
title: Types de données nouveaux et modifiés
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
TQID: 'https://experienceleague.adobe.com/LI8xzlS2eACzYqcV3krzThLm77-z6imYLohPRCTHIYs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 1%

---

# Types de données : nouveaux et modifiés{#data-types-new-and-modified}

Décrit les types nouveaux et modifiés pour l’API IPS version 6.

Syntaxe

## Nouveaux types {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## Types modifiés {#section-56b834b1a3b843279d8715b4a4f3890b}

**Ajouté**

* Ajout de `numUrls` à `UploadUrlsJob`.

* `fileName` ajoutée à `Asset.`

* Ajout de `isHidden` à `MetadataField`.

* Ajout de `taskState` à `TaskProgress`.

* Ajout de `exportJob` à `ActiveJob` et `ScheduledJob`.

* Ajout de `optmizedPath` et `optimizedFile` à `PsdInfo`.

* `contextHandle` ajoutée à :

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Ajout des paramètres suivants à `Asset` :

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Modifié**

* En `User`, a remplacé `role` par `defaultRole`.

* En `Folder`, a remplacé `permissions` par `permissionsSetHandle`.

* En `AssetSummary`, `type` et `name` sont désormais facultatifs.
