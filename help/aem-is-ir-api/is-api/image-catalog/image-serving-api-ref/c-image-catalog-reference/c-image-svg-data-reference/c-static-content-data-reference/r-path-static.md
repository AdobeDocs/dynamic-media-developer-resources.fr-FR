---
title: Chemin
description: Le serveur utilise les règles de résolution de chemin pour trouver le fichier de données.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
TQID: 'https://experienceleague.adobe.com/775L7-IV3woTDvKztYkHLIS4svwI0CnZ6-UeKXitmY0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 140
ht-degree: 4%

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
