---
description: Taille d’image de rendu par défaut. Le serveur oblige les images de réponse à ne pas dépasser cette largeur et cette hauteur si la requête ne spécifie pas explicitement la taille de  du à l’aide de wid= ou hei=.
seo-description: Taille d’image de rendu par défaut. Le serveur oblige les images de réponse à ne pas dépasser cette largeur et cette hauteur si la requête ne spécifie pas explicitement la taille de  du à l’aide de wid= ou hei=.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 27574811-a920-4e54-8635-5a643b8655ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DefaultPix{#defaultpix}

Taille d’image de rendu par défaut. Le serveur oblige les images de réponse à ne pas dépasser cette largeur et cette hauteur si la requête ne spécifie pas explicitement la taille de  du à l’aide de wid= ou hei=.

## Propriétés {#section-9dc5474fc75842308796ab6440b29611}

Deux nombres entiers, 0 ou plus, séparés par une virgule. Largeur et hauteur en pixels. L’une ou l’autre des valeurs peut être définie sur 0 pour ne pas être contrainte.

Ne s’applique pas aux requêtes imbriquées/incorporées.

## Par défaut {#section-1935781c561e4679aa87a5bcced8df90}

Héritée de `default::DefaultPix` si non définie ou si vide.

## Voir aussi {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
