---
description: Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.
seo-description: Détails d’avertissement ou d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
feature: Dynamic Media Classic, SDK/API, Métadonnées
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 8%

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

