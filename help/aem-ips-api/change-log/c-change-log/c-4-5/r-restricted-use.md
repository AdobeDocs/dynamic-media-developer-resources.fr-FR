---
description: Ces opérations et types de données nouveaux ou modifiés disponibles dans le WSDL bêta ne doivent pas être utilisés en dehors des applications développées par Dynamic Media.
solution: Experience Manager
title: Utilisation restreinte
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Utilisation restreinte{#restricted-use}

Ces opérations et types de données nouveaux ou modifiés disponibles dans le WSDL bêta ne doivent pas être utilisés en dehors des applications développées par Dynamic Media.

Ces opérations et types peuvent être désactivés, modifiés ou obsolètes lors des mises à jour système ultérieures.

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

* Modification du `ActiveJob` pour inclure un type de `createVideoSitemapJob`

* Modification du `ScheduledJob` pour inclure un type de `createVideoSitemapJob`

* Modification du `ImageServingPublishJob` pour inclure un `contextHandle` facultatif

* Modification du `ImageRenderingPublishJob` pour inclure un `contextHandle` facultatif

* Modification du `MetadataField` pour inclure un `initialTagField` facultatif

* Modification du `MetadataCondition` pour inclure un paramètre de `caseSensitive` facultatif

* Modification du `PropertySet` pour inclure un `PermissionArray` facultatif en tant que `permissions`

* Modification du `UploadDirectoryJob` afin d’inclure des paramètres facultatifs `xmpKeywords`, `xmpTemplateId` et `xmpTemplateOverride`

* Modification du `VideoPublishJob` pour inclure un `contextHandle` facultatif

**Opérations modifiées**

* Modification du `createAssetSet` pour inclure un `thumbAssetHandle` facultatif

* Modification du `createImageSet` pour inclure un `thumbAssetHandle` facultatif

* Modification du `createMetadataField` pour inclure un paramètre de `initialTagValue` facultatif

* Modification du `createPropertySet` pour inclure un `PermissionUpdateArray` facultatif en tant que `permissionArray`

* Modification du `getImageServingPublishSettings` pour inclure un paramètre de `contextHandle` facultatif

* Modification du `getImageRenderingPublishSettings` pour inclure un paramètre de `contextHandle` facultatif

* Modification du `searchAssetsByFullText` afin d’inclure une série de paramètres facultatifs :

   * `SearchFilter` comme paramètre `filters`

   * `sortBy`
   * `sortDirection`

* Modification du `searchAssetsByMetadata` afin d’inclure une série de paramètres facultatifs :

   * `SearchFilter` comme paramètre `filters`

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` séquence de sept paramètres

* Modification du `setAssetPublishState` pour inclure un `HandleArray` facultatif en tant que `contextHandleArray`

* Modification du `setImageServingPublishSettings` pour inclure un paramètre de `contextHandle` facultatif

* Modification du `setImageRenderingPublishSettings` pour inclure un `contextHandle`paramètre facultatif

* Modification du `submitJob` pour inclure un type de tâche `createVideoSitemap` facultatif
