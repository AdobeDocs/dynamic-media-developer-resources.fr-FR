---
description: Options de fichier PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

Options de fichier PostScript.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| processus | `xsd:string` | Choix du processus PostScript. |
| résolution | `xsd:double` | Résolution du fichier. |
| colorspace | `xsd:string` | Mode Espace colorimétrique PostScript. |
| alpha | `xsd:boolean` | Indique s’il faut pixelliser le fichier dans une image. Si tel est le cas, cela crée un arrière-plan transparent si le fichier d’origine est défini de cette manière. Généralement utilisé pour créer des logos superposés. |
| extractSearchWords | `xsd:boolean` | Extraction ou non des mots de recherche à partir du fichier PostScript. |
