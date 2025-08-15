---
title: Champs des métadonnées de ressource
description: Renvoie les définitions des champs de métadonnées pour les types de ressource spécifiés.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

Renvoie les définitions des champs de métadonnées pour les types de ressource spécifiés.

Syntaxe

## Paramètres {#section-5ad771540c5f40c187b35e34aac19305}

| Nom | Type | Description |
|---|---|---|
| Type de ressource | `xsd:string` | Type de ressource associé aux définitions de champ (voir « Types de ressources » pour connaître les valeurs). |
| Tableau de champs | `types:MetadataFieldArray` | Tableau des définitions de champs de métadonnées associé au type de ressource spécifié dans `assetType`. |
