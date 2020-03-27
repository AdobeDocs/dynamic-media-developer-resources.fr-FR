---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 4.5.
seo-description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 4.5.
seo-title: Opérations nouvelles et modifiées
solution: Experience Manager
title: Opérations nouvelles et modifiées
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Opérations : Nouveau et modifié{#operations-new-and-modified}

Décrit les méthodes d&#39;opérations nouvelles et modifiées pour l&#39;API IPS version 4.5.

Syntaxe

## Nouvelles opérations {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## Opérations modifiées {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` inclut `animatedGifInfo`, `swcInfo`, `cssInfo`et `javascriptInfo` des paramètres.

* `createMetadataField` inclut un `isHidden` paramètre facultatif.

* `saveMetadataField` inclut un `isHidden` paramètre facultatif.

* `searchAssets`
* 
* Le `renameFiles` paramètre a été abandonné pour les versions précédentes et supprimé de l’ `renameAsset` opération. Le chemin d’accès au fichier virtuel est modifié pour correspondre au nouveau nom de fichier (en conservant l’extension de fichier), tandis que les chemins d’accès au fichier physique ne sont pas affectés. Les clients API doivent supprimer les références à ce paramètre lors de la mise à jour vers la nouvelle version de l’API.

