---
description: Décrit les types de données nouveaux et modifiés pour l’API IPS version 4.5.
solution: Experience Manager
title: Types de données nouveaux et modifiés
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 3%

---

# Types de données : Nouveautés et modifications{#data-types-new-and-modified}

Décrit les types de données nouveaux et modifiés pour l’API IPS version 4.5.

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

* La ressource comprend un nouveau champ `fileName` qui renvoie le nom du fichier virtuel.
* `AssetSummary` renvoie un  `type` champ et  `name` 

* `MetadataField` inclut `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` nécessite un  `urlArray` et ajoute un  `numUrls` nombre facultatif
