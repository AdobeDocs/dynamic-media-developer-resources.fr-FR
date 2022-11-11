---
description: Options de fichier du PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 11%

---

# [!DNL PDFOptions]{#pdfoptions}

Options de fichier du PDF.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| processus | `xsd:string` | Choix des &quot;processus PDF&quot;. |
| résolution | `xsd:double` | Résolution du fichier. |
| Espace colorimétrique | `xsd:string` | Choix du mode Colorspace post-script. |
| pdfCatalog | `xsd:boolean` | Il est possible de combiner plusieurs PDF de page dans un catalogue électronique après le rendu (la valeur par défaut est true). |
| extractSearchWords | `xsd:boolean` | Extraction ou non des mots de recherche à partir du fichier du PDF. |
| extractLinks | `xsd:boolean` | Extraction ou non de liens de PDF dans des zones cliquables affectées aux pages pixellisées dans IPS. |
