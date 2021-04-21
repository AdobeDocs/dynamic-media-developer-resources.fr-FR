---
description: Décrit les types de données nouveaux et modifiés pour l'API IPS version 4.5.
solution: Experience Manager
title: Types de données nouveaux et modifiés
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 2%

---


# Types de données : Nouveau et modifié{#data-types-new-and-modified}

Décrit les types de données nouveaux et modifiés pour l&#39;API IPS version 4.5.

Syntaxe

## Nouveaux types {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## Types modifiés {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* Le fichier comprend un nouveau champ `fileName` qui renvoie le nom du fichier virtuel.
* `AssetSummary` renvoie un  `type` champ et  `name` un champ

* `MetadataField` inclut `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` nécessite un  `urlArray` et ajoute un  `numUrls` nombre facultatif

