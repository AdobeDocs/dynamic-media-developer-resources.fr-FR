---
description: Met à jour le champ d’image associé à une ressource d’image.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Met à jour le champ d’image associé à une ressource d’image.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| assetHandle | `xsd:string` | Poignée de ressource. |
| [!DNL resolution] | `xsd:double` | Résolution de l’image en pixels par pouce. |
| [!DNL anchorX] | `xsd:int` | ancre d’image de l’axe X. |
| [!DNL anchorY] | `xsd:int` | ancre d’image de l’axe Y. |
| [!DNL userData] | `xsd:string` | Valeur de `userData` champ de métadonnées, qui est publié dans le champ de catalogue de données utilisateur de diffusion d’images. |
