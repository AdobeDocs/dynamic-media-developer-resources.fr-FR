---
description: Chemin
solution: Experience Manager
title: Chemin
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 5%

---


# Chemin{#path}

Le serveur utilise les règles de résolution de chemin décrites dans [Gestion des données source](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) pour trouver le fichier de données.

## Propriétés {#section-72d9edc532ad43349afcb4df22e1c692}

Chaîne de texte. Obligatoire pour les enregistrements d’image et SVG, peut être vide pour les enregistrements de modèle. S’il est spécifié, il doit s’agir d’un chemin d’accès au fichier Image Server relatif ou absolu valide. attribute::DefaultExt est ajouté si aucun suffixe de fichier n’est présent.

## Formats de fichier image pris en charge {#section-8d6443c883aa48aaa00316fe9661aaa8}

Reportez-vous à la description de l’utilitaire Image Converter (IC) pour obtenir une liste complète des formats de fichier image pris en charge.

Les applications qui nécessitent des données d’image de plusieurs résolutions différentes seront plus performantes lors de l’utilisation du format de résolution multiple TIFF (PTIFF) de la pyramide Dynamic Media. L’utilitaire IC permet de créer des images PTIFF à partir de n’importe quel format d’image pris en charge.

## Par défaut {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Aucune

## Voir aussi {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[Utilitaire](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b) IC,  [attribut::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [attribut::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
