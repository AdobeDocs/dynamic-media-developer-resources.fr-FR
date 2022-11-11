---
description: Propriétés du fichier PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

Propriétés du fichier PostScript.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| [!DNL engine] | `xsd:string` | Moteur de génération utilisé (voir &quot;Informations sur la génération&quot; pour les valeurs). |
| [!DNL originator] | `types:Asset` | Enregistrement de la ressource Principale utilisée dans la génération. |
| [!DNL generated] | `types:Asset` | Enregistrement de la ressource générée. |
| attributeArray | `types:GenerationAttributeArray` | Tableau d’attributs associés au processus de génération. |
