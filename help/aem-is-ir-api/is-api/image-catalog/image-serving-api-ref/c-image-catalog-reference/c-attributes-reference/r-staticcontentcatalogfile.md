---
description: Chemins d’accès aux fichiers de données du catalogue de contenu statique. Indique les fichiers qui contiennent les données de contenu statique pour ce catalogue.
solution: Experience Manager
title: StaticContentCatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 4%

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
