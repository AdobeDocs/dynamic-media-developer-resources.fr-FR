---
description: Options de fichier PostScript.
seo-description: Options de fichier PostScript.
seo-title: PostScriptOptions
solution: Experience Manager
title: PostScriptOptions
topic: Dynamic Media Image Production System API
uuid: 31526bfe-b651-47a8-98c0-2750a3d9cabf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 11%

---


# PostScriptOptions{#postscriptoptions}

Options de fichier PostScript.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`processus`*` | `xsd:string` | Choix du processus PostScript. |
| `*`résolution`*` | `xsd:double` | Résolution du fichier. |
| `*`Espace colorimétrique`*` | `xsd:string` | Mode d’espace colorimétrique PostScript. |
| `*`alpha`*` | `xsd:boolean` | Indique si le fichier doit être pixellisé dans une image. Si tel est le cas, il crée un arrière-plan transparent si le fichier d’origine est défini de cette manière. Généralement utilisé pour créer des logos superposés. |
| `*`extractSearchWords`*` | `xsd:boolean` | Extrait ou non des mots recherchés dans le fichier PostScript. |

