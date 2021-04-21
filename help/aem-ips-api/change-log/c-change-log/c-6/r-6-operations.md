---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 6.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 1%

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

**Ajouté**

* Ajouté `isHidden` et `initialTagValue` à :

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Ajouté `thumbAssetHandle` à :

   * `createImageSet`
   * `createAssetSet`

   Ajouté `companyHandle` à :

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Ajouté `contextHandle` à :

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* includeInactif Ajouté à :

   * `getUsers`.
   * `getUserChars`.

* Ajouté `permissionArray` à `createPropertySet`.

* Ajouté `exportJob` à `submitJob`.

**Modifié**

* Dans `addUser` et `setUser`, `role` a été remplacé par `defaultRole`.

* Dans `getCompanyMembers`, `userArray` a été remplacé par `memberArray`.

* Dans `getCompanyMembership`, `companyArray` a été remplacé par `membershipArray`.

* Dans `addUser`, `setCompanyMembership` et `addCompanyMembership`, `membershipArray` a été remplacé par `companyHandleArray`.

* Dans `getCompanyMembership`, `companyArray` a été remplacé par `membershipArray`.

* Dans `getUserChars`, `includeInvalid` est désormais facultatif.

**Supprimé**

* Suppression de `renameFiles` de `renameAsset`.

* Suppression de `getXMPPanelViewDefinition`.
* Suppression de `searchAssetsByFulltext` et `searchAssetsBySimilarity`.

