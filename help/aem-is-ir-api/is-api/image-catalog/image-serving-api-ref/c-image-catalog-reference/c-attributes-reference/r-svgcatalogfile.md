---
description: Chemins d’accès aux fichiers de données SVG. Indique les fichiers contenant les données SVG pour ce catalogue.
solution: Experience Manager
title: SvgCatalogFile
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 4%

---


# SvgCatalogFile{#svgcatalogfile}

Chemins d’accès aux fichiers de données SVG. Indique les fichiers contenant les données SVG pour ce catalogue.

Les fichiers de données SVG sont chargés après tous les fichiers de données image, dans l’ordre exact spécifié. Si la même valeur `catalog::Id` se produit dans plusieurs enregistrements (dans la même image ou des fichiers de catalogue SVG différents), la dernière instance prévaut.

## Propriétés {#section-fc2d549f76474792837b2b92ec2087ea}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Facultatif. Chaque valeur doit être un chemin d’accès ou un chemin d’accès absolu au fichier par rapport au dossier de catalogue.

## Par défaut {#section-a4e58951f3c249599665b823566433c9}

Vide, ce qui indique que ce catalogue d’images n’inclut aucune donnée SVG.

## Voir aussi {#section-dad6cf4cc5994cf5bbed8807c96119dd}

[Données](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29) du catalogue,  [CatalogFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-catalogfile.md#reference-16498bb4cb33458697c1ab002ea8db79)
