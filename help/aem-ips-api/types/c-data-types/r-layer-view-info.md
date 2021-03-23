---
description: Propriétés de la vue de calques.
seo-description: Propriétés de la vue de calques.
seo-title: LayerViewInfo
solution: Experience Manager
title: LayerViewInfo
uuid: 58d26f4d-03a6-4f57-bc8e-117355c0d74c
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 10%

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

