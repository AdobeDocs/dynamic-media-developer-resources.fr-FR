---
description: Ces opérations et types de données nouveaux ou modifiés disponibles dans le fichier WSDL bêta ne doivent pas être utilisés en dehors des applications développées Scene7.
seo-description: Ces opérations et types de données nouveaux ou modifiés disponibles dans le fichier WSDL bêta ne doivent pas être utilisés en dehors des applications développées Scene7.
seo-title: Utilisation restreinte
solution: Experience Manager
title: Utilisation restreinte
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Utilisation restreinte{#restricted-use}

Ces opérations et types de données nouveaux ou modifiés disponibles dans le fichier WSDL bêta ne doivent pas être utilisés en dehors des applications développées Scene7.

Ces opérations et types peuvent être désactivés, modifiés ou abandonnés avec les mises à jour système suivantes.

**Nouveaux types**

* AssetPublishContextes
* AssetPublishContextesArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* Contexte de publication
* PublishContextArray
* SearchFilter
* LongArray

**Nouvelles opérations**

* applyMetadataTemplate
* batchGetAssetPublishContextes
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContextes
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

* Modification `ActiveJob` pour inclure un `createVideoSitemapJob` type

* Modification `ScheduledJob` pour inclure un `createVideoSitemapJob` type

* Changement `ImageServingPublishJob` pour inclure une `contextHandle`

* Changement `ImageRenderingPublishJob` pour inclure une `contextHandle`

* Changement `MetadataField` pour inclure une `initialTagField`

* Changement `MetadataCondition` pour inclure et `caseSensitive` paramètre facultatif

* Modification `PropertySet` pour inclure une option `PermissionArray` en tant que `permissions`

* Modification `UploadDirectoryJob` pour inclure des paramètres facultatifs `xmpKeywords`, `xmpTemplateId` et `xmpTemplateOverride`

* Changement `VideoPublishJob` pour inclure une `contextHandle`

**Opérations modifiées**

* Changement `createAssetSet` pour inclure une `thumbAssetHandle`

* Changement `createImageSet` pour inclure une `thumbAssetHandle`

* Modification `createMetadataField` pour inclure un `initialTagValue` paramètre facultatif

* Modification `createPropertySet` pour inclure une option `PermissionUpdateArray` en tant que `permissionArray`

* Modification `getImageServingPublishSettings` pour inclure un `contextHandle` paramètre facultatif

* Modification `getImageRenderingPublishSettings` pour inclure un `contextHandle` paramètre facultatif

* Modification `searchAssetsByFullText` pour inclure une série de paramètres facultatifs :

   * `SearchFilter` comme `filters` paramètre

   * `sortBy`
   * `sortDirection`

* Modification `searchAssetsByMetadata` pour inclure une série de paramètres facultatifs :

   * `SearchFilter` comme `filters` paramètre

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` séquence de sept paramètres

* Modification `setAssetPublishState` pour inclure une option `HandleArray` en tant que `contextHandleArray`

* Modification `setImageServingPublishSettings` pour inclure un `contextHandle` paramètre facultatif

* Modification `setImageRenderingPublishSettings` pour inclure un `contextHandle`paramètre facultatif

* Modification `submitJob` pour inclure un type de `createVideoSitemap` tâche facultatif

