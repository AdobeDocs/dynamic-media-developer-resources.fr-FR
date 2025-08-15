---
description: Chemins d’accès aux fichiers de données du catalogue de contenu statique. Spécifie les fichiers contenant les données de contenu statique pour ce catalogue.
solution: Experience Manager
title: Fichier de catalogue de contenu statique
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 2%

---

# Fichier de catalogue de contenu statique{#staticcontentcatalogfile}

Chemins d’accès aux fichiers de données du catalogue de contenu statique. Spécifie les fichiers contenant les données de contenu statique pour ce catalogue.

Contenu statique Les fichiers de données de catalogue sont chargés dans l’ordre indiqué. Si la même `static::Id` valeur apparaît dans plusieurs enregistrements (dans le même fichier de catalogue ou dans des fichiers de catalogue différents), la dernière instance prévaut.

## Propriétés {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Optionnel. Chaque valeur doit être un chemin absolu de fichier ou un chemin relatif au dossier du catalogue.

## Par défaut {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vide qui indique que ce catalogue d’images n’inclut aucune donnée de contenu statique.

## Voir aussi {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Données de catalogue](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
