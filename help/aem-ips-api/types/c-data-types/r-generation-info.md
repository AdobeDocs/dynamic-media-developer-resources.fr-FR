---
description: Propriétés de fichier PostScript.
seo-description: Propriétés de fichier PostScript.
seo-title: GenerationInfo
solution: Experience Manager
title: GenerationInfo
topic: Dynamic Media Image Production System API
uuid: 166637e5-b981-4f64-8d92-5fce4f1b20d2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 13%

---


# GenerationInfo{#generationinfo}

Propriétés de fichier PostScript.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`moteur`*` | `xsd:string` | Moteur de génération utilisé (voir &quot;Informations de génération&quot; pour les valeurs). |
| `*`initiateur`*` | `types:Asset` | Enregistrement de l’actif Principal utilisé dans la génération. |
| `*`généré`*` | `types:Asset` | Enregistrement de l’actif généré. |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | Tableau des attributs associés au processus de génération. |

