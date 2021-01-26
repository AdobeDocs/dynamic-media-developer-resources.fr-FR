---
description: Options de fichier PDF.
seo-description: Options de fichier PDF.
seo-title: Options PDFO
solution: Experience Manager
title: Options PDFO
topic: Dynamic Media Image Production System API
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 9%

---


# PDFOoptions{#pdfoptions}

Options de fichier PDF.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`processus`*` | `xsd:string` | Choix des &quot;processus PDF&quot;. |
| `*`résolution`*` | `xsd:double` | Résolution du fichier. |
| `*`Espace colorimétrique`*` | `xsd:string` | Choix du mode Colorspace post-script. |
| `*`pdfCatalog`*` | `xsd:boolean` | Combinaison d’un PDF de plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). |
| `*`extractSearchWords`*` | `xsd:boolean` | Extrait ou non des mots recherchés dans le fichier PDF. |
| `*`extractLinks`*` | `xsd:boolean` | Extrait ou non des liens PDF dans des zones cliquables affectées aux pages pixellisées dans IPS. |

