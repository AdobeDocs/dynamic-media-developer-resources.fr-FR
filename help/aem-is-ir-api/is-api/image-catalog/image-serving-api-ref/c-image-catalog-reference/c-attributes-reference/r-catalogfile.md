---
description: Chemins d’accès au fichier de données image. Indique les fichiers contenant les données image pour ce catalogue.
seo-description: Chemins d’accès au fichier de données image. Indique les fichiers contenant les données image pour ce catalogue.
seo-title: CatalogFile
solution: Experience Manager
title: CatalogFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 3599c8d3-dc4b-434e-8b11-775ea6f155ee
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CatalogFile{#catalogfile}

Chemins d’accès au fichier de données image. Indique les fichiers contenant les données image pour ce catalogue.

Les fichiers de données image sont chargés dans l’ordre spécifié. Si la même `catalog::Id` valeur se produit dans plusieurs enregistrements (que ce soit dans le même fichier de catalogue ou dans des fichiers de catalogue différents), la dernière instance prévaut.

## Propriétés {#section-6da55f145ecd4e31a5de52637a436983}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Facultatif. Chaque valeur doit être un chemin d’accès ou un chemin d’accès absolu au fichier par rapport au dossier du catalogue.

## Par défaut {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vide, ce qui indique que ce catalogue d’images n’inclut aucune donnée d’image.

## Voir aussi {#section-910b67c5041d44d99a105ad43ff63a37}

[Champs de données du catalogue](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
