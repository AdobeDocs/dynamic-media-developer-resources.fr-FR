---
description: Renvoie les définitions de champs de métadonnées pour les types de ressource spécifiés.
seo-description: Renvoie les définitions de champs de métadonnées pour les types de ressource spécifiés.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Media Classic, SDK/API, Métadonnées, Gestion des ressources
role: Développeur, Administrateur
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---


# AssetMetadataFields{#assetmetadatafields}

Renvoie les définitions de champs de métadonnées pour les types de ressource spécifiés.

Syntaxe

## Paramètres {#section-5ad771540c5f40c187b35e34aac19305}

| Nom | Type | Description |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Type d’actif associé aux définitions de champ (voir Types d’actif pour les valeurs). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Tableau des définitions de champs de métadonnées associées au type de ressource spécifié dans `assetType`. |

