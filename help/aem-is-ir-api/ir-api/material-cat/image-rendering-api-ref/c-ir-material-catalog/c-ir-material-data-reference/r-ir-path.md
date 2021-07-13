---
description: Chemin du fichier image. Chemin d’accès relatif et nom d’un fichier de texture ou d’image décorative.
solution: Experience Manager
title: Chemin *
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# Chemin *{#path}

Chemin du fichier image. Chemin d’accès relatif et nom d’un fichier de texture ou d’image décorative.

Le serveur combine cette valeur avec `attribute::RootPath` pour créer le chemin d’accès au fichier image réel. Peut également être un chemin absolu.

Utilisé pour spécifier le fichier image de texture pour les matériaux de texture, de vitrine et de vitrine, ainsi que le fichier image RVB ou RVBA pour les matériaux de bordure décale et mur. Toutes les armoires et les fenêtres recouvrant les matériaux ne nécessitent pas une image de texture répétable distincte.

## Propriétés {#section-8c12ea24f21d4472be677581893e6681}

Chaîne de texte. Requis pour les matériaux de texture et de décal, optionnel pour les matériaux de vitrine et de vitrine. S’il est spécifié, il doit s’agir d’un chemin d’accès au fichier relatif ou absolu valide. Doit être vide pour les matériaux couleur solides.

## Formats de fichiers pris en charge {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Le rendu d’image prend en charge les mêmes formats d’image source que le service d’images Dynamic Media.

Les applications qui nécessitent des données d’image à plusieurs résolutions différentes seront plus performantes lors de l’utilisation du format PTIFF (Dynamic Media pyramid TIFF) à plusieurs résolutions. La diffusion d’images comprend l’utilitaire Image Converter (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Pour obtenir la liste complète des formats de fichiers pris en charge, reportez-vous à la description de l’utilitaire IC dans la documentation du serveur d’images .

## Par défaut {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Aucune

## Voir aussi {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilitaire IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [attribut::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
