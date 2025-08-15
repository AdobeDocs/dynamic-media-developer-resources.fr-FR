---
description: Objet de stockage de fichiers ou de ressources hiérarchique. Les dossiers peuvent contenir un (ou plusieurs) sous-dossier.
solution: Experience Manager
title: Dossier
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 8%

---

# [!DNL Folder]{#folder}

Objet de stockage de fichiers ou de ressources hiérarchique. Les dossiers peuvent contenir un (ou plusieurs) sous-dossier.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| poignée de dossier | `xsd:string` | Poignée de dossier. |
| [!DNL path] | `xsd:string` | Chemin d’accès du dossier. |
| Dernière modification | `xsd:dateTime` | Date de dernière modification. |
| childLastModified | `xsd:dateTime` | Date de dernière modification des sous-dossiers et des ressources enfants du dossier. |
| permissionsSetHandle | `xsd:string` | Gestion des autorisations de dossier. |
| hasSubfolder | `types:Boolean` | Détermine si un dossier comporte des sous-dossiers. |
| SubfolderArray | `types:FolderArray` | Tableau de sous-dossiers dans un dossier. |
