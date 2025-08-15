---
title: Mise à jour AssetContextStateUpdate
description: Définissez un nouveau jeu d’indicateurs d’état de publication pour le contexte de publication associé à une ressource.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 4%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

Définissez un nouveau jeu d’indicateurs d’état de publication pour le contexte de publication associé à une ressource.

**Paramètres**

| Nom | Type | Description |
|---|---|---|
| AssetHandle | `xsd:string` | Gérez la ressource à mettre à jour. |
| Mise à jour contextuelle | `types:ContextStateUpdateArray` | Tableau des états de contact de publication pour la ressource à mettre à jour. |
