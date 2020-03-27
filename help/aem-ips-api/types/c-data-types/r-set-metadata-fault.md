---
description: Avertissement ou détails d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.
seo-description: Avertissement ou détails d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Scene7 Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SetMetadataFault{#setmetadatafault}

Avertissement ou détails d’erreur pour une mise à jour d’utilisation dans une opération batchSetAssetMetadata.

Syntaxe

## Paramètres {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nom | Type | Description |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Fichier dont les métadonnées ont été définies sans succès. |
| ` *`fieldHandle`*` | `xsd:string` | Identifiant du champ de métadonnées dont la valeur a été définie sans succès. |
| ` *`code`*` | `xsd:int` | Code d&#39;erreur. |
| ` *`motif`*` | `xsd:string` | Description de l’erreur (texte brut). |

