---
description: Décrit les méthodes d’opérations nouvelles et modifiées pour l’API IPS version 4.5.
solution: Experience Manager
title: Opérations nouvelles et modifiées
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: d2e73ae5f92d9ba3471dc7207842753ccff94c28
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Opérations : Nouveautés et modifications{#operations-new-and-modified}

Décrit les méthodes d’opérations nouvelles et modifiées pour l’API IPS version 4.5.

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

* `Asset` inclut  `animatedGifInfo`,  `swcInfo`,  `cssInfo` et  `javascriptInfo` des paramètres.
* `createMetadataField` inclut un  `isHidden` paramètre facultatif.
* `saveMetadataField` inclut un  `isHidden` paramètre facultatif.
* `searchAssets`
* Le paramètre `renameFiles` a été abandonné pour les versions antérieures et supprimé de l’opération `renameAsset`. Le chemin d’accès au fichier virtuel est modifié pour correspondre au nouveau nom de la ressource (en conservant l’extension du fichier), tandis que les chemins d’accès aux fichiers physiques ne sont pas affectés. Les clients API doivent supprimer les références à ce paramètre lors de la mise à jour vers la nouvelle version de l’API.
