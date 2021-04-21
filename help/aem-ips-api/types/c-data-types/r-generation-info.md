---
description: Propriétés de fichier PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

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

