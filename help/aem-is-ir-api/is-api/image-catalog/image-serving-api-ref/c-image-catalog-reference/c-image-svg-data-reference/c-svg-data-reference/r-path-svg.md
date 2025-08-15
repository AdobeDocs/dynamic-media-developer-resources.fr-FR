---
description: Chemin
solution: Experience Manager
title: Chemin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f2d17309-c4d0-477f-a8d8-b40f05a1a60b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 5%

---

# Chemin{#path}

Le serveur utilise les règles de résolution de chemin d’accès décrites dans la section [Gestion des données Source](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) pour rechercher le fichier de données.

## Propriétés {#section-72d9edc532ad43349afcb4df22e1c692}

Chaîne de texte. Obligatoire pour les enregistrements d’image et SVG, peut être vide pour les enregistrements de modèle. S’il est spécifié, il doit s’agir d’un chemin d’accès relatif ou absolu au fichier Image Server valide. attribute::DefaultExt est ajouté si aucun suffixe de fichier n&#39;est présent.

## Formats de fichiers image pris en charge {#section-8d6443c883aa48aaa00316fe9661aaa8}

Reportez-vous à la description de l’utilitaire Convertisseur d’images (IC) pour obtenir une liste complète des formats de fichiers image pris en charge.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes ont de meilleures performances lors de l’utilisation du format multi-résolution Dynamic Media pyramid TIFF (PTIFF). L’utilitaire IC permet de créer des images PTIFF à partir de n’importe quel format d’image pris en charge.

## Par défaut {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Aucune

## Voir aussi {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[Utilitaire IC](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [attribute::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [attribute::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0), [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
