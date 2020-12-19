---
description: Chemin d’accès au fichier image.
solution: Experience Manager
title: Chemin
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 7b837020deef888a038a074d0aa826d43e60aeb6
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# Chemin{#path}

Chemin d’accès au fichier image.

Chemin d’accès relatif ou absolu et nom du fichier image source associé à cet enregistrement de catalogue. Le serveur utilise les règles de résolution de chemin décrites dans la section Gestion des données source pour trouver le fichier de données.

## Propriétés {#path-properties}

Chaîne de texte. Obligatoire pour les enregistrements d’image, peut être vide pour les enregistrements de modèle. S’il est spécifié, il doit s’agir d’un chemin d’accès au fichier Image Server relatif ou absolu valide. attribute::DefaultExt est ajouté si aucun suffixe de fichier n’est présent.

## Formats de fichier image pris en charge {#path-supported-image-file-formats}

Reportez-vous à la description de l’utilitaire Image Converter (IC) pour obtenir une liste complète des formats de fichier pris en charge.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes s’exécuteront mieux lors de l’utilisation du format PTIFF (Dynamic Media pyramid TIFF) à plusieurs résolutions. L’utilitaire IC permet de créer des images PTIFF à partir de n’importe quel format d’image pris en charge.

## Par défaut {#path-default}

Aucune

## Voir aussi {#path-seealso}

[Utilitaire](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)  IC,  [attribut::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [attribut::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->