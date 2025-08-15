---
description: Met à jour le champ d’image associé à une ressource image.
solution: Experience Manager
title: Mise à jour du champ d’image
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Met à jour le champ d’image associé à une ressource image.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| AssetHandle | `xsd:string` | Gestion des ressources. |
| [!DNL resolution] | `xsd:double` | Résolution d’image en pixels par pouce. |
| [!DNL anchorX] | `xsd:int` | Ancrage d’image de l’axe X. |
| [!DNL anchorY] | `xsd:int` | Ancre d’image de l’axe Y. |
| [!DNL userData] | `xsd:string` | Valeur du champ de métadonnées qui est publiée dans le champ du catalogue de données utilisateur serveur d’images `userData` . |
