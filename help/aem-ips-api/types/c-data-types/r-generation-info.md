---
description: Propriétés du fichier PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 12%

---

# GenerationInfo{#generationinfo}

Propriétés du fichier PostScript.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`moteur`*` | `xsd:string` | Moteur de génération utilisé (voir &quot;Informations sur la génération&quot; pour les valeurs). |
| `*`originator`*` | `types:Asset` | Enregistrement de la ressource Principale utilisée dans la génération. |
| `*`généré`*` | `types:Asset` | Enregistrement de la ressource générée. |
| `*`attributeArray`*` | `types:GenerationAttributeArray` | Tableau d’attributs associés au processus de génération. |
