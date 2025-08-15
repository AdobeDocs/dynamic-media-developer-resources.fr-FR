---
description: Chemins des fichiers de données d’image. Spécifie les fichiers contenant les données image pour ce catalogue.
solution: Experience Manager
title: Fichier catalogue
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 2%

---

# Fichier catalogue{#catalogfile}

Chemins des fichiers de données d’image. Spécifie les fichiers contenant les données image pour ce catalogue.

Les fichiers de données image sont chargés dans l’ordre indiqué. Si la même `catalog::Id` valeur apparaît dans plusieurs enregistrements (dans le même fichier de catalogue ou dans des fichiers de catalogue différents), la dernière instance prévaut.

## Propriétés {#section-6da55f145ecd4e31a5de52637a436983}

Une ou plusieurs valeurs de chaîne de texte, séparées par des virgules. Optionnel. Chaque valeur doit être un chemin absolu de fichier ou un chemin relatif au dossier du catalogue.

## Par défaut {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vide qui indique que ce catalogue d’images ne contient aucune donnée image.

## Voir aussi {#section-910b67c5041d44d99a105ad43ff63a37}

[Champs de données de catalogue](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
