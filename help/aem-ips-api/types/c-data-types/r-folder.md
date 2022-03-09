---
description: Objet de stockage de fichier ou de ressource hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.
solution: Experience Manager
title: Dossier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# Dossier{#folder}

Objet de stockage de fichier ou de ressource hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| folderHandle | `xsd:string` | Poignée de dossier. |
| chemin | `xsd:string` | Chemin du dossier. |
| lastModified | `xsd:dateTime` | Date de la dernière modification. |
| childLastModified | `xsd:dateTime` | Date de dernière modification pour les sous-dossiers et les ressources enfants de dossier. |
| permissionsSetHandle | `xsd:string` | Gestion des autorisations de dossier. |
| hasSubfolder | `types:Boolean` | Détermine si un dossier contient des sous-dossiers. |
| subfolderArray | `types:FolderArray` | Tableau de sous-dossiers dans un dossier. |
