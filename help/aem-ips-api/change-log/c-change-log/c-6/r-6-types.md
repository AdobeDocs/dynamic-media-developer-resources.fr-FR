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

**Ajout**

* Ajout `numUrls` à `UploadUrlsJob`.

* Ajout `fileName` à `Asset.`

* Ajout `isHidden` à `MetadataField`.

* Ajout `taskState` à `TaskProgress`.

* Ajout `exportJob` à `ActiveJob` et `ScheduledJob`.

* Ajout `optmizedPath` et `optimizedFile` à `PsdInfo`.

* Ajout `contextHandle` à :

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Ajout des paramètres suivants à `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Modifié**

* En `User`1999, `role` il a été remplacé par `defaultRole`.

* En `Folder`1999, `permissions` il a été remplacé par `permissionsSetHandle`.

* Dans `AssetSummary`, `type` et `name` sont maintenant facultatifs.

