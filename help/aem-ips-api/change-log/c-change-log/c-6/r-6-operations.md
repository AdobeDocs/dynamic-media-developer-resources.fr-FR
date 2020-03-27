---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 6.
seo-description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 6.
seo-title: Opérations nouvelles et modifiées
solution: Experience Manager
title: Opérations nouvelles et modifiées
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Opérations : Nouveau et modifié{#operations-new-and-modified}

Décrit les méthodes d&#39;opérations nouvelles et modifiées pour l&#39;API IPS version 6.

Syntaxe

## Nouvelles opérations {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Opérations modifiées {#section-f4e8755527444266ae806e3f4c851ae6}

**Ajout**

* Ajout `isHidden` et `initialTagValue` à :

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Ajout `thumbAssetHandle` à :

   * `createImageSet`
   * `createAssetSet`
   Ajout `companyHandle` à :

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`
   Ajout `contextHandle` à :

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* Ajout de includeInactive à :

   * `getUsers`.
   * `getUserChars`.

* Ajout `permissionArray` à `createPropertySet`.

* Ajout `exportJob` à `submitJob`.

**Modifié**

* Dans `addUser` et `setUser`, changé `role` en `defaultRole`.

* En `getCompanyMembers`1999, `userArray` il a été remplacé par `memberArray`.

* En `getCompanyMembership`1999, `companyArray` il a été remplacé par `membershipArray`.

* Dans `addUser`, `setCompanyMembership`, et `addCompanyMembership`, changé `membershipArray` en `companyHandleArray`.

* En `getCompanyMembership`1999, `companyArray` il a été remplacé par `membershipArray`.

* Dans `getUserChars`, `includeInvalid` est désormais facultatif.

**Supprimé**

* Supprimé `renameFiles` de `renameAsset`.

* Removed `getXMPPanelViewDefinition`.
* Supprimé `searchAssetsByFulltext` et `searchAssetsBySimilarity`.

