---
description: Taille d’image de rendu par défaut. Le serveur limite la largeur et la hauteur des images de réponse si la requête ne spécifie pas explicitement la taille de la vue à l’aide de wid= ou hei=.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 3%

---


# DefaultPix{#defaultpix}

Taille d’image de rendu par défaut. Le serveur limite la largeur et la hauteur des images de réponse si la requête ne spécifie pas explicitement la taille de la vue à l’aide de wid= ou hei=.

## Propriétés {#section-9dc5474fc75842308796ab6440b29611}

Deux nombres entiers, 0 ou plus, séparés par une virgule. Largeur et hauteur en pixels. L’une ou l’autre des valeurs peut être définie sur 0 pour ne pas être contrainte.

Ne s’applique pas aux requêtes imbriquées/incorporées.

## Par défaut {#section-1935781c561e4679aa87a5bcced8df90}

Hérité de `default::DefaultPix` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [attribut::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
