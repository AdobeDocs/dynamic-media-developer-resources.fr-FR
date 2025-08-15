---
description: Décrit les méthodes d’opérations nouvelles et modifiées pour l’API IPS version 6.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# Opérations : nouvelles et modifiées{#operations-new-and-modified}

Décrit les méthodes d’opérations nouvelles et modifiées pour l’API IPS version 6.

Syntaxe

## Nouvelles opérations {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Opérations modifiées {#section-f4e8755527444266ae806e3f4c851ae6}

**Supplémentaire**

* Ajouté `isHidden` et `initialTagValue` à :

   * `saveMetadataField`
   * ` `updateMetadataField&#39;&#39;
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

* Ajout d’includeInactive à :

   * `getUsers`.
   * `getUserChars`.

* Ajouté `permissionArray` à `createPropertySet`.

* Ajouté `exportJob` à `submitJob`.

**Changé**

* Dans `addUser` et `setUser`, remplacé `role` par `defaultRole`.

* Dans `getCompanyMembers`, remplacé `userArray` par `memberArray`.

* Dans `getCompanyMembership`, remplacé `companyArray` par `membershipArray`.

* Dans `addUser`, `setCompanyMembership`et `addCompanyMembership`, remplacé `membershipArray` par `companyHandleArray`.

* Dans `getCompanyMembership`, remplacé `companyArray` par `membershipArray`.

* Dans `getUserChars`, `includeInvalid` est désormais facultatif.

**Enlevé**

* Supprimé `renameFiles` de `renameAsset`.

* Supprimé `getXMPPanelViewDefinition`.
* Supprimé `searchAssetsByFulltext` et `searchAssetsBySimilarity`.
