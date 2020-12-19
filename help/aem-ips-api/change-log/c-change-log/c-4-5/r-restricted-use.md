---
description: Ces opérations et types de données nouveaux ou modifiés disponibles dans la version bêta du WSDL ne doivent pas être utilisés en dehors des applications développées par Scene7.
seo-description: Ces opérations et types de données nouveaux ou modifiés disponibles dans la version bêta du WSDL ne doivent pas être utilisés en dehors des applications développées par Scene7.
seo-title: Utilisation restreinte
solution: Experience Manager
title: Utilisation restreinte
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---


# Utilisation restreinte{#restricted-use}

Ces opérations et types de données nouveaux ou modifiés disponibles dans la version bêta du WSDL ne doivent pas être utilisés en dehors des applications développées par Scene7.

Ces opérations et types peuvent être désactivés, modifiés ou abandonnés avec les mises à jour suivantes du système.

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

* Modification de `ActiveJob` pour inclure un type `createVideoSitemapJob`

* Modification de `ScheduledJob` pour inclure un type `createVideoSitemapJob`

* Modification de `ImageServingPublishJob` pour inclure un `contextHandle` facultatif

* Modification de `ImageRenderingPublishJob` pour inclure un `contextHandle` facultatif

* Modification de `MetadataField` pour inclure un `initialTagField` facultatif

* Modification de `MetadataCondition` en incluant et en optant pour le paramètre `caseSensitive`

* `PropertySet` a été modifié pour inclure un `PermissionArray` facultatif comme `permissions`

* Modification des paramètres `UploadDirectoryJob` pour inclure les paramètres facultatifs `xmpKeywords`, `xmpTemplateId` et `xmpTemplateOverride`

* Modification de `VideoPublishJob` pour inclure un `contextHandle` facultatif

**Opérations modifiées**

* Modification de `createAssetSet` pour inclure un `thumbAssetHandle` facultatif

* Modification de `createImageSet` pour inclure un `thumbAssetHandle` facultatif

* Modification de `createMetadataField` pour inclure un paramètre facultatif `initialTagValue`

* `createPropertySet` a été modifié pour inclure un `PermissionUpdateArray` facultatif comme `permissionArray`

* Modification de `getImageServingPublishSettings` pour inclure un paramètre facultatif `contextHandle`

* Modification de `getImageRenderingPublishSettings` pour inclure un paramètre facultatif `contextHandle`

* Modification de `searchAssetsByFullText` pour inclure une série de paramètres facultatifs :

   * `SearchFilter` comme  `filters` paramètre

   * `sortBy`
   * `sortDirection`

* Modification de `searchAssetsByMetadata` pour inclure une série de paramètres facultatifs :

   * `SearchFilter` comme  `filters` paramètre

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` séquence de sept paramètres

* `setAssetPublishState` a été modifié pour inclure un `HandleArray` facultatif comme `contextHandleArray`

* Modification de `setImageServingPublishSettings` pour inclure un paramètre facultatif `contextHandle`

* Modification de `setImageRenderingPublishSettings` pour inclure un paramètre `contextHandle`facultatif

* Modification de `submitJob` pour inclure un type de tâche `createVideoSitemap` facultatif

