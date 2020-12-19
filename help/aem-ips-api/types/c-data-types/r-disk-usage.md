---
description: Statistiques d'espace disque pour un fichier ou un dossier.
seo-description: Statistiques d'espace disque pour un fichier ou un dossier.
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Scene7 Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---


# DiskUsage{#diskusage}

Statistiques d&#39;espace disque pour un fichier ou un dossier.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Poignée de société. |
| ` *`companyName`*` | `xsd:string` | Nom de la société. |
| ` *`imageCount`*` | `xsd:int` | Nombre d’images stockées. |
| ` *`diskSpaceUsage`*` | `xsd:long` | Total des fichiers côté fichier en kilo-octets. |
| ` *`lastModified`*` | `xsd:dateTime` | Date, heure et fuseau horaire de la dernière modification du type `DiskUsage`. |

