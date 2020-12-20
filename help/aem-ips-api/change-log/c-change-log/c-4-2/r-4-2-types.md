---
description: Décrit les types de données nouveaux et modifiés pour l'API IPS version 4.2.
seo-description: Décrit les types de données nouveaux et modifiés pour l'API IPS version 4.2.
seo-title: Types de données nouveaux et modifiés
solution: Experience Manager
title: Types de données nouveaux et modifiés
topic: Scene7 Image Production System API
uuid: 274e49da-9eb8-4082-971c-056acb47a53e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 2%

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

