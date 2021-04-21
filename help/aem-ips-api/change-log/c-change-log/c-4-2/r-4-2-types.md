---
description: Décrit les types de données nouveaux et modifiés pour l'API IPS version 4.2.
solution: Experience Manager
title: Types de données nouveaux et modifiés
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
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

