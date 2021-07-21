---
description: Options de fichier PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 9%

---

# PDFOptions{#pdfoptions}

Options de fichier PDF.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`processus`*` | `xsd:string` | Choix des &quot;processus PDF&quot;. |
| `*`resolution`*` | `xsd:double` | Résolution du fichier. |
| `*`Espace colorimétrique`*` | `xsd:string` | Choix du mode Colorspace post-script. |
| `*`pdfCatalog`*` | `xsd:boolean` | Si vous souhaitez combiner un PDF de plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). |
| `*`extractSearchWords`*` | `xsd:boolean` | Extraction ou non des mots de recherche à partir du fichier PDF. |
| `*`extractLinks`*` | `xsd:boolean` | Extraction ou non de liens PDF dans des zones cliquables affectées aux pages pixelisées dans IPS. |
