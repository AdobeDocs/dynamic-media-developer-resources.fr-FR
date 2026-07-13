---
description: Options du fichier PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

Options du fichier PDF.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| processus | `xsd:string` | Choix des « processus PDF ». |
| résolution | `xsd:double` | Résolution du fichier. |
| colorspace | `xsd:string` | Choix du mode Colorspace post-script. |
| pdfCatalog | `xsd:boolean` | Permet de combiner un PDF de plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). |
| extractSearchWords | `xsd:boolean` | Extraction de mots de recherche à partir du fichier PDF |
| extractLinks | `xsd:boolean` | Extraction de liens PDF dans des zones cliquables affectées aux pages pixellisées dans IPS. |

