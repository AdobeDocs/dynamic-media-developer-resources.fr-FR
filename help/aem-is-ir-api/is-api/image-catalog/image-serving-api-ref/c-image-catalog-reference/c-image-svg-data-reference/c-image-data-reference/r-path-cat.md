---
description: Chemin du fichier image.
solution: Experience Manager
title: Chemin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---

# Chemin{#path}

Chemin du fichier image.

Chemin relatif ou absolu et nom du fichier image source associé à cet enregistrement de catalogue. Le serveur utilise les règles de résolution de chemin décrites dans la section Gestion des données source pour trouver le fichier de données.

## Propriétés {#path-properties}

Chaîne de texte. Requis pour les enregistrements d’image, peut être vide pour les enregistrements de modèle. S’il est spécifié, il doit s’agir d’un chemin d’accès au fichier Image Server relatif ou absolu valide. attribute::DefaultExt est ajouté si aucun suffixe de fichier n’est présent.

## Formats de fichier image pris en charge {#path-supported-image-file-formats}

Reportez-vous à la description de l’utilitaire de conversion d’images (IC) pour obtenir la liste complète des formats de fichiers pris en charge.

Les applications qui nécessitent des données d’image à plusieurs résolutions différentes sont les plus performantes lors de l’utilisation du format PTIFF (Dynamic Media pyramid TIFF) à résolution multiple. L’utilitaire IC est utilisé pour créer des images PTIFF à partir de n’importe quel format d’image pris en charge.

## Par défaut {#path-default}

Aucune

## Voir aussi {#path-seealso}

[Utilitaire IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
