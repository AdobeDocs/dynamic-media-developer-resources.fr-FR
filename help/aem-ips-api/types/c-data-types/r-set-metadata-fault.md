---
description: Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic, SDK/API, Métadonnées
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 10%

---


# SetMetadataFault{#setmetadatafault}

Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Fichier dont les métadonnées ont été définies sans succès. |
| `*`fieldHandle`*` | `xsd:string` | Poignée du champ de métadonnées dont la valeur a été définie sans succès. |
| `*`code`*` | `xsd:int` | Code d&#39;erreur. |
| `*`motif`*` | `xsd:string` | Description de la défaillance (texte brut). |

