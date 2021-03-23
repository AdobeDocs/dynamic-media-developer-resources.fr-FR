---
description: Objet d’enregistrement de fichier ou de fichier hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.
seo-description: Objet d’enregistrement de fichier ou de fichier hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.
seo-title: Dossier
solution: Experience Manager
title: Dossier
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# Dossier{#folder}

Objet d’enregistrement de fichier ou de fichier hiérarchique. Les dossiers peuvent contenir un ou plusieurs sous-dossiers.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Poignée de dossier. |
| `*`chemin`*` | `xsd:string` | Chemin du dossier. |
| `*`lastModified`*` | `xsd:dateTime` | Date de la dernière modification. |
| `*`childLastModified`*` | `xsd:dateTime` | Date de dernière modification des sous-dossiers et des dossiers des ressources enfants. |
| `*`permissionsSetHandle`*` | `xsd:string` | Poignée des autorisations de dossier. |
| `*`hasSubfolder`*` | `types:Boolean` | Détermine si un dossier comporte des sous-dossiers. |
| `*`subfolderArray`*` | `types:FolderArray` | Tableau de sous-dossiers dans un dossier. |

