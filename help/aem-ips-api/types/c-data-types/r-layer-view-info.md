---
description: Propriétés de la vue de calques.
solution: Experience Manager
title: LayerViewInfo
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 11%

---


# LayerViewInfo{#layerviewinfo}

Propriétés de la vue de calques.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`url`*` | `xsd:string` | URL du serveur d’images qui représente le modèle. Combine les champs `urlModifier` et `urlPostAp- plyModifier`. |
| `*`urlModificateur`*` | `xsd:string` | Commandes de protocole de traitement des images à appliquer avant les commandes request ou `urlPostApplyModifier`. |
| `*`urlPostApplyModificateur`*` | `xsd:string` | Commandes de protocole de traitement des images à appliquer après `urlModifier` et les commandes de requête. |

