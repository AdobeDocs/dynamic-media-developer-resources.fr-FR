---
description: Statistiques sur l’espace disque pour une ressource ou un dossier.
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 14%

---

# [!DNL DiskUsage]{#diskusage}

Statistiques sur l’espace disque pour une ressource ou un dossier.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| companyHandle | `xsd:string` | Poignée de la société. |
| companyName | `xsd:string` | Nom de la société. |
| imageCount | `xsd:int` | Nombre d’images stockées. |
| diskSpaceUsage | `xsd:long` | Côté fichier total en kilo-octets. |
| lastModified | `xsd:dateTime` | Date, heure et fuseau horaire de la variable `DiskUsage` a été modifié pour la dernière fois. |
