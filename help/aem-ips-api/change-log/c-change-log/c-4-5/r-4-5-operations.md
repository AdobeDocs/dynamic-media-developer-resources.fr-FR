---
description: Décrit les méthodes d'opérations nouvelles et modifiées pour l'API IPS version 4.5.
solution: Experience Manager
title: Opérations - Nouvelles et modifiées
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: 'https://experienceleague.adobe.com/n4U8LW8otIaBBDalW1wRJFaweTAw3-0Sh0ckgIEADAI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 1%

---

# Opérations : nouvelles et modifiées{#operations-new-and-modified}

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

* `Asset` inclut les paramètres `animatedGifInfo`, `swcInfo`, `cssInfo` et `javascriptInfo`.
* `createMetadataField` comprend un paramètre de `isHidden` facultatif.
* `saveMetadataField` comprend un paramètre de `isHidden` facultatif.
* `searchAssets`
* Le paramètre `renameFiles` a été abandonné pour les versions antérieures et supprimé de l’opération `renameAsset`. Le chemin d’accès au fichier virtuel est modifié pour correspondre au nouveau nom de ressource (en préservant l’extension de fichier), tandis que les chemins d’accès aux fichiers physiques ne sont pas affectés. Les clients d’API doivent supprimer les références à ce paramètre lors de la mise à jour vers la nouvelle version de l’API.
