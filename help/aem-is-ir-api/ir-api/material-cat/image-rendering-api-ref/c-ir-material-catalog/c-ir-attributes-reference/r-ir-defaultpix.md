---
description: Taille d’image de rendu par défaut. Le serveur oblige les images de réponse à ne pas dépasser cette largeur et cette hauteur si la requête ne spécifie pas la taille d’affichage explicitement à l’aide de wid= ou hei=.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

Taille d’image de rendu par défaut. Le serveur oblige les images de réponse à ne pas dépasser cette largeur et cette hauteur si la requête ne spécifie pas la taille d’affichage explicitement à l’aide de wid= ou hei=.

## Propriétés {#section-9dc5474fc75842308796ab6440b29611}

Deux nombres entiers, 0 ou plus, séparés par une virgule. Largeur et hauteur en pixels. L’une ou l’autre des valeurs (ou les deux) peuvent être définies sur 0 pour ne pas être contraintes.

Non applicable aux requêtes imbriquées/incorporées.

## Par défaut {#section-1935781c561e4679aa87a5bcced8df90}

Hérité de `default::DefaultPix` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
