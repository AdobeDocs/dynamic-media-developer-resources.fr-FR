---
description: Chemin du fichier image. Chemin d’accès relatif et nom d’un fichier d’image de texture ou de décalcomanie.
solution: Experience Manager
title: Chemin*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 1%

---

# Chemin*{#path}

Chemin du fichier image. Chemin d’accès relatif et nom d’un fichier d’image de texture ou de décalcomanie.

Le serveur associe cette valeur pour `attribute::RootPath` créer le chemin d’accès réel au fichier image. Peut également être un chemin absolu.

Permet de spécifier le fichier image de texture pour les matériaux de texture, d’armoire et de garniture de fenêtre, et le fichier image RVB ou RVBA pour les matériaux de décalcomanie et de bordure murale. Tous les matériaux d’armoire et de couvre-fenêtre ne nécessitent pas une image de texture reproductible distincte.

## Propriétés {#section-8c12ea24f21d4472be677581893e6681}

Chaîne de texte. Requis pour les matériaux de texture et de décalcomanie, facultatif pour les matériaux d’armoire et de couvre-fenêtres. S’il est spécifié, il doit s’agir d’un chemin d’accès de fichier relatif ou absolu valide. Doit être vide pour les matériaux de couleur unie.

## Formats de fichiers pris en charge {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Image Rendering prend en charge les mêmes formats d’image source qu Dynamic Media image Server.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes fonctionnent mieux lors de l’utilisation du format multi-résolution Dynamic Media pyramid TIFF (PTIFF). Image Serving inclut l’utilitaire Image Converter (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Reportez-vous à la description de l’utilitaire IC dans la documentation Image Serving pour obtenir la liste complète des formats de fichiers pris en charge.

## Par défaut {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Aucune

## Voir aussi {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilitaire](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) [IC, attribute ::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
