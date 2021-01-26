---
description: Entrée dans un fichier ZIP.
seo-description: Entrée dans un fichier ZIP.
seo-title: EntréeZip
solution: Experience Manager
title: EntréeZip
topic: Dynamic Media Image Production System API
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 12%

---


# ZipEntry{#zipentry}

Entrée dans un fichier ZIP.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`name`*` | `xsd:string` | Nom de l’entrée. |
| `*`isDirectory`*` | `xsd:boolean` | Détermine si l’entrée est un répertoire. |
| `*`lastModified`*` | `xsd:dateTime` | Date et heure de la dernière modification. |
| `*`compresséSize`*` | `xsd:long` | Taille compressée. |
| `*`uncompresséSize`*` | `xsd:long` | Taille non compressée. |

