---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 6.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
TQID: 'https://experienceleague.adobe.com/DLA26IsxxpZ0TSSfQBrvZSl8mbcJCaTfnpK-bhhmglg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 1%

---

# Opérations : nouvelles et modifiées{#operations-new-and-modified}

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

* `isHidden` et `initialTagValue` ajoutés à :

   * `saveMetadataField`
   * ` `updateMetadataField«
   * `createMetadataField`

* `thumbAssetHandle` ajoutée à :

   * `createImageSet`
   * `createAssetSet`

  `companyHandle` ajoutée à :

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  `contextHandle` ajoutée à :

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* Ajout de la mention includeInactive à :

   * `getUsers`.
   * `getUserChars`.

* Ajout de `permissionArray` à `createPropertySet`.

* Ajout de `exportJob` à `submitJob`.

**Modifié**

* En `addUser` et `setUser`, a modifié `role` en `defaultRole`.

* En `getCompanyMembers`, a remplacé `userArray` par `memberArray`.

* En `getCompanyMembership`, a remplacé `companyArray` par `membershipArray`.

* En `addUser`, `setCompanyMembership` et `addCompanyMembership`, a modifié `membershipArray` en `companyHandleArray`.

* En `getCompanyMembership`, a remplacé `companyArray` par `membershipArray`.

* En `getUserChars`, `includeInvalid` est désormais facultatif.

**Supprimé**

* A supprimé `renameFiles` de `renameAsset`.

* A Supprimé `getXMPPanelViewDefinition`.
* Suppression de `searchAssetsByFulltext` et `searchAssetsBySimilarity`.
