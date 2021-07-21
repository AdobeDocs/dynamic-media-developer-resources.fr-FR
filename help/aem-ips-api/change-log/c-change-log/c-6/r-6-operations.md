---
description: Décrit les nouvelles méthodes d’exploitation et les méthodes modifiées pour l’API IPS version 6.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 1%

---

# Opérations : Nouveautés et modifications{#operations-new-and-modified}

Décrit les nouvelles méthodes d’exploitation et les méthodes modifiées pour l’API IPS version 6.

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

* Ajout de `isHidden` et `initialTagValue` à :

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Ajout de `thumbAssetHandle` à :

   * `createImageSet`
   * `createAssetSet`

   Ajout de `companyHandle` à :

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Ajout de `contextHandle` à :

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* Ajout de includeInactive à :

   * `getUsers`.
   * `getUserChars`.

* Ajout de `permissionArray` à `createPropertySet`.

* Ajout de `exportJob` à `submitJob`.

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
