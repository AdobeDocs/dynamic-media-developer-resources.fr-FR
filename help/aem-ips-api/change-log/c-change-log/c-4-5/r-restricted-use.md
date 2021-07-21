---
description: Ces opérations et types de données nouveaux ou modifiés disponibles dans le fichier WSDL bêta ne doivent pas être utilisés en dehors des applications développées par Dynamic Media.
solution: Experience Manager
title: Utilisation limitée
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Utilisation limitée{#restricted-use}

Ces opérations et types de données nouveaux ou modifiés disponibles dans le fichier WSDL bêta ne doivent pas être utilisés en dehors des applications développées par Dynamic Media.

Ces opérations et types d’opération peuvent être désactivés, modifiés ou obsolètes avec les mises à jour suivantes du système.

**Nouveaux types**

* AssetPublishContexts
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Nouvelles opérations**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Types modifiés**

* Modification de `ActiveJob` pour inclure un type `createVideoSitemapJob`

* Modification de `ScheduledJob` pour inclure un type `createVideoSitemapJob`

* Modification de `ImageServingPublishJob` afin d’inclure un `contextHandle` facultatif.

* Modification de `ImageRenderingPublishJob` afin d’inclure un `contextHandle` facultatif.

* Modification de `MetadataField` afin d’inclure un `initialTagField` facultatif.

* Modification du `MetadataCondition` en incluant et en option le paramètre `caseSensitive`

* `PropertySet` a été modifié pour inclure un `PermissionArray` facultatif comme `permissions`

* Modification des `UploadDirectoryJob` pour inclure les paramètres facultatifs `xmpKeywords`, `xmpTemplateId` et `xmpTemplateOverride`.

* Modification de `VideoPublishJob` afin d’inclure un `contextHandle` facultatif.

**Opérations modifiées**

* Modification de `createAssetSet` afin d’inclure un `thumbAssetHandle` facultatif.

* Modification de `createImageSet` afin d’inclure un `thumbAssetHandle` facultatif.

* Modification de `createMetadataField` pour inclure un paramètre `initialTagValue` facultatif.

* `createPropertySet` a été modifié pour inclure un `PermissionUpdateArray` facultatif comme `permissionArray`

* Modification de `getImageServingPublishSettings` pour inclure un paramètre `contextHandle` facultatif.

* Modification de `getImageRenderingPublishSettings` pour inclure un paramètre `contextHandle` facultatif.

* Modification de `searchAssetsByFullText` afin d’inclure une série de paramètres facultatifs :

   * `SearchFilter` comme  `filters` paramètre

   * `sortBy`
   * `sortDirection`

* Modification de `searchAssetsByMetadata` afin d’inclure une série de paramètres facultatifs :

   * `SearchFilter` comme  `filters` paramètre

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` séquence de sept paramètres

* `setAssetPublishState` a été modifié pour inclure un `HandleArray` facultatif comme `contextHandleArray`

* Modification de `setImageServingPublishSettings` pour inclure un paramètre `contextHandle` facultatif.

* Modification de `setImageRenderingPublishSettings` pour inclure un paramètre `contextHandle`facultatif.

* Modification de `submitJob` pour inclure un type de tâche `createVideoSitemap` facultatif.
