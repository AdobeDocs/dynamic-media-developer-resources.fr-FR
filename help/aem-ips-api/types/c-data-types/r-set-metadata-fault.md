---
description: Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---

# SetMetadataFault{#setmetadatafault}

Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| assetHandle | `xsd:string` | La ressource dont les métadonnées ont été définies sans succès. |
| fieldHandle | `xsd:string` | Gestion du champ de métadonnées dont la valeur a été définie sans succès. |
| code | `xsd:int` | Code de défaillance. |
| motif | `xsd:string` | Description des défauts (texte brut). |
