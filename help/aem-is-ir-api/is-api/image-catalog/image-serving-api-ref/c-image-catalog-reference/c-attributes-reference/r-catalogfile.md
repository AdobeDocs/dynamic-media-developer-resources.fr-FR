---
description: Chemins du fichier de données image. Indique les fichiers qui contiennent les données image pour ce catalogue.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 4%

---


# CatalogFile{#catalogfile}

Chemins du fichier de données image. Indique les fichiers qui contiennent les données image pour ce catalogue.

Les fichiers de données image sont chargés dans l’ordre spécifié. Si la même valeur `catalog::Id` se produit dans plusieurs enregistrements (dans le même fichier catalogue ou dans des fichiers de catalogue différents), la dernière instance prévaut.

## Propriétés {#section-6da55f145ecd4e31a5de52637a436983}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Facultatif. Chaque valeur doit être un chemin d’accès ou un chemin d’accès absolu au fichier par rapport au dossier de catalogue.

## Par défaut {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vide, ce qui indique que ce catalogue d’images n’inclut aucune donnée d’image.

## Voir aussi {#section-910b67c5041d44d99a105ad43ff63a37}

[Champs de données du catalogue](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
