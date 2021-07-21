---
description: Décrit les types de données nouveaux et modifiés pour l’API IPS version 4.2.
solution: Experience Manager
title: Types de données nouveaux et modifiés
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 3%

---

# Types de données : Nouveautés et modifications{#data-types-new-and-modified}

Décrit les types de données nouveaux et modifiés pour l’API IPS version 4.2.

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
