---
description: Renvoie les définitions de champs de métadonnées pour les types de ressources spécifiés.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Métadonnées,Gestion des ressources
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# AssetMetadataFields{#assetmetadatafields}

Renvoie les définitions de champs de métadonnées pour les types de ressources spécifiés.

Syntaxe

## Paramètres {#section-5ad771540c5f40c187b35e34aac19305}

| Nom | Type | Description |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Type de ressource associé aux définitions de champ (voir &quot;Types de ressources&quot; pour les valeurs). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Tableau des définitions de champ de métadonnées associées au type de ressource spécifié dans `assetType`. |
