---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 4.5.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

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

* `Asset` inclut  `animatedGifInfo`,  `swcInfo`,  `cssInfo`et  `javascriptInfo` paramètres.

* `createMetadataField` inclut un  `isHidden` paramètre facultatif.

* `saveMetadataField` inclut un  `isHidden` paramètre facultatif.

* `searchAssets`
* 
* Le paramètre `renameFiles` a été abandonné pour les versions antérieures et supprimé de l&#39;opération `renameAsset`. Le chemin d’accès au fichier virtuel est modifié pour correspondre au nouveau nom de fichier (en conservant l’extension de fichier), tandis que les chemins d’accès aux fichiers physiques ne sont pas affectés. Les clients d’API doivent supprimer les références à ce paramètre lors de la mise à jour vers la nouvelle version de l’API.

