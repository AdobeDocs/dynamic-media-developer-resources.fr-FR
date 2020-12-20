---
description: Décrit les types nouveaux et modifiés pour l'API IPS version 6.
seo-description: Décrit les types nouveaux et modifiés pour l'API IPS version 6.
seo-title: Types de données nouveaux et modifiés
solution: Experience Manager
title: Types de données nouveaux et modifiés
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 1%

---


# Types de données : Nouveau et modifié{#data-types-new-and-modified}

Décrit les types nouveaux et modifiés pour l&#39;API IPS version 6.

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

* Ajouté `numUrls` à `UploadUrlsJob`.

* `fileName` Ajouté à `Asset.`

* Ajouté `isHidden` à `MetadataField`.

* Ajouté `taskState` à `TaskProgress`.

* Ajouté `exportJob` à `ActiveJob` et `ScheduledJob`.

* Ajouté `optmizedPath` et `optimizedFile` à `PsdInfo`.

* Ajouté `contextHandle` à :

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Ajouté les paramètres suivants à `Asset` :

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Modifié**

* Dans `User`, `role` a été remplacé par `defaultRole`.

* Dans `Folder`, `permissions` a été remplacé par `permissionsSetHandle`.

* Dans `AssetSummary`, `type` et `name` sont désormais facultatifs.

