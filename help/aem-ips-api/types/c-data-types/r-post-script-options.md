---
description: Options du fichier PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 13%

---

# PostScriptOptions{#postscriptoptions}

Options du fichier PostScript.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| processus | `xsd:string` | Choix du processus PostScript. |
| résolution | `xsd:double` | Résolution du fichier. |
| Espace colorimétrique | `xsd:string` | Mode colorspace PostScript. |
| alpha | `xsd:boolean` | Indique s’il faut pixelliser le fichier dans une image. Si tel est le cas, il crée un arrière-plan transparent si le fichier d’origine est défini de cette manière. Généralement utilisé pour créer des logos superposés. |
| extractSearchWords | `xsd:boolean` | Extraction ou non des mots de recherche à partir du fichier PostScript. |
