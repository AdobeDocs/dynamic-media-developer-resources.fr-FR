---
description: Propriétés du mode Calque.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 13%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Propriétés du mode Calque.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| url | `xsd:string` | URL du serveur d’images qui représente le modèle. Combine les champs `urlModifier` et `urlPostAp- plyModifier`. |
| urlModifier | `xsd:string` | Commandes du protocole de diffusion d’images à appliquer avant les commandes de requête ou de `urlPostApplyModifier`. |
| urlPostApplyModifier | `xsd:string` | Commandes du protocole de diffusion d’images à appliquer après les commandes `urlModifier` et de requête. |
