---
description: Décrit les types de données nouveaux et modifiés pour l'API IPS version 4.2.
solution: Experience Manager
title: Types de données nouveaux et modifiés
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---


# Types de données : Nouveau et modifié{#data-types-new-and-modified}

Décrit les types de données nouveaux et modifiés pour l&#39;API IPS version 4.2.

Syntaxe

## Nouveaux types {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## Types modifiés {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Fichier**

Paramètres ajoutés :

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

Paramètres supprimés :

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

Paramètres ajoutés :

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

Paramètres ajoutés :

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

Paramètres ajoutés :

* `preservePublishState`
* `preserveCrop`

