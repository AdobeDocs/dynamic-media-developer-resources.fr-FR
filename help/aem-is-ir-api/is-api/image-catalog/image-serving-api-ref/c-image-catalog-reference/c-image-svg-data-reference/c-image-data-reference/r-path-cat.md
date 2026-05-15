---
description: Chemin du fichier image.
solution: Experience Manager
title: Chemin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
TQID: 'https://experienceleague.adobe.com/dpQY2E7P1LzEhYg05p6C5MQRvx9jgdMB-GrBReIIqig'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 4%

---

# Chemin{#path}

Chemin du fichier image.

Chemin d’accès relatif ou absolu et nom du fichier image source associé à cet enregistrement de catalogue. Le serveur utilise les règles de résolution de chemin d’accès décrites dans la section Gestion des données Source pour rechercher le fichier de données.

## Propriétés {#path-properties}

Chaîne de texte. Obligatoire pour les enregistrements d’image, peut être vide pour les enregistrements de modèle. S’il est spécifié, il doit s’agir d’un chemin d’accès relatif ou absolu au fichier Image Server valide. attribute::DefaultExt est ajouté si aucun suffixe de fichier n&#39;est présent.

## Formats De Fichiers Image Pris En Charge {#path-supported-image-file-formats}

Consultez la description de l’utilitaire Convertisseur d’images (IC) pour obtenir la liste complète des formats de fichiers pris en charge.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes ont de meilleures performances lors de l’utilisation du format multi-résolution Dynamic Media pyramid TIFF (PTIFF). L’utilitaire IC permet de créer des images PTIFF à partir de n’importe quel format d’image pris en charge.

## Par défaut {#path-default}

Aucune

## Voir aussi {#path-seealso}

[Utilitaire IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
