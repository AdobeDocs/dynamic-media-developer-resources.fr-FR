---
description: Chemin d’accès au fichier image. Chemin d’accès relatif et nom d’un fichier image de texture ou de décale.
solution: Experience Manager
title: Chemin *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---


# Chemin *{#path}

Chemin d’accès au fichier image. Chemin d’accès relatif et nom d’un fichier image de texture ou de décale.

Le serveur combine cette valeur avec `attribute::RootPath` pour créer le chemin d’accès au fichier image réel. Peut aussi être un chemin absolu.

Utilisé pour spécifier le fichier d’image de texture pour les matériaux de texture, les armoires et les garnitures de fenêtre, ainsi que le fichier d’image RVB ou RVB pour les matériaux de bordure de décal et de paroi. Tous les matériaux de recouvrement de l&#39;armoire et de la fenêtre ne nécessitent pas une image de texture répétable distincte.

## Propriétés {#section-8c12ea24f21d4472be677581893e6681}

Chaîne de texte. Obligatoire pour les matériaux de texture et de décal, optionnel pour les matériaux de garnissage des armoires et des fenêtres. S&#39;il est spécifié, il doit s&#39;agir d&#39;un chemin d&#39;accès au fichier relatif ou absolu valide. Doit être vide pour les matériaux de couleur unie.

## Formats de fichiers pris en charge {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Le rendu d’images prend en charge les mêmes formats d’image source que le service d’images Dynamic Media.

Les applications qui nécessitent des données d’image de plusieurs résolutions différentes seront plus performantes lors de l’utilisation du format de résolution multiple TIFF (PTIFF) de la pyramide Dynamic Media. Image Serving inclut l’utilitaire Image Converter (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Pour obtenir une liste complète des formats de fichiers pris en charge, reportez-vous à la description de l’utilitaire IC dans la documentation sur la diffusion d’images.

## Par défaut {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Aucune

## Voir aussi {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilitaire](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md)  IC,  [attribut::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
