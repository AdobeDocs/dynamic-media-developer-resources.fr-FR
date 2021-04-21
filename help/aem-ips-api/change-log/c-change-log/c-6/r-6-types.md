---
description: Décrit les types nouveaux et modifiés pour l'API IPS version 6.
solution: Experience Manager
title: Types de données nouveaux et modifiés
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
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

