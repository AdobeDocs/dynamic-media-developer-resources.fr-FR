---
description: Propriétés d’affichage des calques.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 12%

---

# LayerViewInfo{#layerviewinfo}

Propriétés d’affichage des calques.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| url | `xsd:string` | URL du serveur d’images qui représente le modèle. Combinaisons `urlModifier` et `urlPostAp- plyModifier` champs. |
| urlModifier | `xsd:string` | Commandes du protocole de diffusion d’images à appliquer avant la demande ou `urlPostApplyModifier` des commandes. |
| urlPostApplyModifier | `xsd:string` | Commandes du protocole de diffusion d’images à appliquer après `urlModifier` et les commandes de requête. |
