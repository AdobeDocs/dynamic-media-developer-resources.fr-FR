---
description: Chemins d’accès aux fichiers de données du catalogue de contenu statique. Indique les fichiers qui contiennent les données de contenu statique pour ce catalogue.
seo-description: Chemins d’accès aux fichiers de données du catalogue de contenu statique. Indique les fichiers qui contiennent les données de contenu statique pour ce catalogue.
seo-title: StaticContentCatalogFile
solution: Experience Manager
title: StaticContentCatalogFile
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 82d2a68a-255a-4e65-a29f-7022e7f0f5ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 3%

---


# StaticContentCatalogFile{#staticcontentcatalogfile}

Chemins d’accès aux fichiers de données du catalogue de contenu statique. Indique les fichiers qui contiennent les données de contenu statique pour ce catalogue.

Les fichiers de données de catalogue de contenu statique sont chargés dans l’ordre spécifié. Si la même valeur `static::Id` se produit dans plusieurs enregistrements (dans le même fichier catalogue ou dans des fichiers de catalogue différents), la dernière instance prévaut.

## Propriétés {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Facultatif. Chaque valeur doit être un chemin d’accès ou un chemin d’accès absolu au fichier par rapport au dossier de catalogue.

## Par défaut {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vide, ce qui indique que ce catalogue d’images n’inclut aucune donnée de contenu statique.

## Voir aussi {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Données du catalogue](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
