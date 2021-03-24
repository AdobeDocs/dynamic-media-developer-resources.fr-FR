---
description: Renvoie les définitions de champs de métadonnées pour les types de ressource spécifiés.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic, SDK/API, Métadonnées, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

Renvoie les définitions de champs de métadonnées pour les types de ressource spécifiés.

Syntaxe

## Paramètres {#section-5ad771540c5f40c187b35e34aac19305}

| Nom | Type | Description |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Type d’actif associé aux définitions de champ (voir Types d’actif pour les valeurs). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Tableau des définitions de champs de métadonnées associées au type de ressource spécifié dans `assetType`. |

