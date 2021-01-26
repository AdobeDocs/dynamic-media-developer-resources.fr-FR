---
description: Décrit les types de données nouveaux et modifiés pour l'API IPS version 4.5.
solution: Experience Manager
title: Types de données nouveaux et modifiés
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

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

