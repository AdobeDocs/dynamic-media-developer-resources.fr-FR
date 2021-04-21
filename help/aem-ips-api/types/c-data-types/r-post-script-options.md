---
description: Options de fichier PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 10%

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

