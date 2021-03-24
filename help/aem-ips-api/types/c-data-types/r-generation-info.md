---
description: Propriétés de fichier PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic, SDK/API
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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

