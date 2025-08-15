---
description: Options des fichiers PDF.
solution: Experience Manager
title: Opérations PDF
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

Options des fichiers PDF.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| processus | `xsd:string` | Choix de « Processus PDF ». |
| résolution | `xsd:double` | Résolution de fichiers. |
| Espace colorimétrique | `xsd:string` | Choix du mode Espace colorimétrique Post-script. |
| Catalogue PDF | `xsd:boolean` | S’il convient de combiner un PDF de plusieurs pages dans un catalogue électronique après le rendu (la valeur par défaut est true). |
| Extraire les mots de recherche | `xsd:boolean` | S’il convient d’extraire des mots de recherche du fichier PDF. |
| Extraire les liens | `xsd:boolean` | S’il faut extraire des liens PDF dans des zones cliquables affectées aux pages pixelisées dans IPS. |
