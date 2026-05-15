---
description: Chemin du fichier image. Chemin d'accès relatif et nom d'une texture ou d'un fichier image de décalque.
solution: Experience Manager
title: Chemin *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
TQID: 'https://experienceleague.adobe.com/ndDZ1MOPM1GHqOKFkwwMnJoZHVjaCeVVEHudb-5fPk0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 208
ht-degree: 1%

---

# Chemin *{#path}

Chemin du fichier image. Chemin d&#39;accès relatif et nom d&#39;une texture ou d&#39;un fichier image de décalque.

Le serveur associe cette valeur à `attribute::RootPath` pour créer le chemin d’accès réel au fichier image. Peut également être un chemin absolu.

Utilisé pour spécifier le fichier image de texture pour les matériaux de texture, d&#39;armoire et de revêtement de fenêtre, et le fichier image RGB ou RGBA pour les matériaux de bordure de mur et de vignette. Tous les matériaux d&#39;armoire et de recouvrement de fenêtre ne nécessitent pas une image de texture répétable distincte.

## Propriétés {#section-8c12ea24f21d4472be677581893e6681}

Chaîne de texte. Requis pour les matériaux de texture et de décalque, en option pour les matériaux d&#39;armoire et de revêtement de fenêtre. S’il est spécifié, il doit s’agir d’un chemin d’accès relatif ou absolu valide. Doit être vide pour les matériaux de couleur unie.

## Formats de fichiers pris en charge {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

Le rendu d’image prend en charge les mêmes formats d’image source que la diffusion d’images Dynamic Media.

Les applications qui nécessitent des données d’image dans plusieurs résolutions différentes ont de meilleures performances lors de l’utilisation du format multi-résolution Dynamic Media pyramid TIFF (PTIFF). La diffusion d’images inclut l’utilitaire Convertisseur d’images (IC) qui crée des images PTIFF à partir de n’importe quel format pris en charge.

Reportez-vous à la description de l’utilitaire IC dans la documentation du service d’images pour obtenir une liste complète des formats de fichiers pris en charge.

## Par défaut {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Aucune

## Voir aussi {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
