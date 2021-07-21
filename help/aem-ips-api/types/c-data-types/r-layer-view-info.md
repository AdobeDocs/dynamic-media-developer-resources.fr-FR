---
description: Propriétés d’affichage des calques.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '52'
ht-degree: 11%

---

# LayerViewInfo{#layerviewinfo}

Propriétés d’affichage des calques.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`url`*` | `xsd:string` | URL du serveur d’images qui représente le modèle. Combine les champs `urlModifier` et `urlPostAp- plyModifier`. |
| `*`urlModifier`*` | `xsd:string` | Commandes du protocole de diffusion d’images à appliquer avant les commandes request ou `urlPostApplyModifier`. |
| `*`urlPostApplyModifier`*` | `xsd:string` | Commandes du protocole de diffusion d’images à appliquer après les commandes `urlModifier` et de requête. |
