---
description: Ces opérations et types de données nouveaux ou modifiés disponibles dans le fichier WSDL bêta ne doivent pas être utilisés en dehors des applications développées par Dynamic Media.
solution: Experience Manager
title: Utilisation limitée
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
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

* Modification de `ImageServingPublishJob` pour inclure un `contextHandle` facultatif

* Modification de `ImageRenderingPublishJob` pour inclure un `contextHandle` facultatif

* Modification de `MetadataField` pour inclure un `initialTagField` facultatif

* Modification du paramètre `MetadataCondition` pour inclure et facultatif `caseSensitive`

* `PropertySet` modifié pour inclure un `PermissionArray` facultatif en `permissions`

* Modification des paramètres `UploadDirectoryJob` pour inclure les paramètres facultatifs `xmpKeywords`, `xmpTemplateId` et `xmpTemplateOverride`.

* Modification de `VideoPublishJob` pour inclure un `contextHandle` facultatif

**Opérations modifiées**

* Modification de `createAssetSet` pour inclure un `thumbAssetHandle` facultatif

* Modification de `createImageSet` pour inclure un `thumbAssetHandle` facultatif

* Modification de `createMetadataField` pour inclure un paramètre `initialTagValue` facultatif.

* `createPropertySet` modifié pour inclure un `PermissionUpdateArray` facultatif en `permissionArray`

* Modification de `getImageServingPublishSettings` pour inclure un paramètre `contextHandle` facultatif.

* Modification de `getImageRenderingPublishSettings` pour inclure un paramètre `contextHandle` facultatif.

* Modification de `searchAssetsByFullText` pour inclure une série de paramètres facultatifs :

   * `SearchFilter` comme paramètre `filters`

   * `sortBy`
   * `sortDirection`

* Modification de `searchAssetsByMetadata` pour inclure une série de paramètres facultatifs :

   * `SearchFilter` comme paramètre `filters`

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` séquence de sept paramètres

* `setAssetPublishState` modifié pour inclure un `HandleArray` facultatif en `contextHandleArray`

* Modification de `setImageServingPublishSettings` pour inclure un paramètre `contextHandle` facultatif.

* Modification de `setImageRenderingPublishSettings` pour inclure un paramètre `contextHandle`facultatif

* Modification de `submitJob` pour inclure un type de tâche `createVideoSitemap` facultatif.
