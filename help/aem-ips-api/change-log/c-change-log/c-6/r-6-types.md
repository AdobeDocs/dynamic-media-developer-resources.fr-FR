---
description: Décrit les types nouveaux et modifiés de l’API IPS version 6.
solution: Experience Manager
title: Types de données nouveaux et modifiés
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 1%

---

# Types de données : Nouveautés et modifications{#data-types-new-and-modified}

Décrit les types nouveaux et modifiés de l’API IPS version 6.

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

**Ajout**

* Ajout de `numUrls` à `UploadUrlsJob`.

* Ajout de `fileName` à `Asset.`

* Ajout de `isHidden` à `MetadataField`.

* Ajout de `taskState` à `TaskProgress`.

* Ajout de `exportJob` à `ActiveJob` et `ScheduledJob`.

* Ajout de `optmizedPath` et `optimizedFile` à `PsdInfo`.

* Ajout de `contextHandle` à :

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Ajout des paramètres suivants à `Asset` :

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Modifié**

* Dans `User`, `role` a été remplacé par `defaultRole`.

* Dans `Folder`, `permissions` a été remplacé par `permissionsSetHandle`.

* Dans `AssetSummary`, `type` et `name` sont désormais facultatifs.
