---
description: Objet d’enregistrement de fichier ou de fichier hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.
seo-description: Objet d’enregistrement de fichier ou de fichier hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.
seo-title: Dossier
solution: Experience Manager
title: Dossier
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 10%

---


# Dossier{#folder}

Objet d’enregistrement de fichier ou de fichier hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Poignée de dossier. |
| ` *`chemin`*` | `xsd:string` | Chemin du dossier. |
| ` *`lastModified`*` | `xsd:dateTime` | Date de la dernière modification. |
| ` *`childLastModified`*` | `xsd:dateTime` | Date de dernière modification des sous-dossiers et des dossiers des ressources enfants. |
| ` *`permissionsSetHandle`*` | `xsd:string` | Poignée des autorisations de dossier. |
| ` *`hasSubfolder`*` | `types:Boolean` | Détermine si un dossier comporte des sous-dossiers. |
| ` *`subfolderArray`*` | `types:FolderArray` | Tableau de sous-dossiers dans un dossier. |

