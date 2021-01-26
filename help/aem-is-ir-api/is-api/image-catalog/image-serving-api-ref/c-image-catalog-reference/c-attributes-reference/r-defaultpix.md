---
description: Taille de vue par défaut.
seo-description: Taille de vue par défaut.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 4%

---


# DefaultPix{#defaultpix}

Taille de vue par défaut.

Le serveur limite la largeur et la hauteur des images de réponse si la requête ne spécifie pas explicitement la taille de la vue à l’aide de `wid=`, `hei=` ou `scl=`.

## Propriétés {#section-c3e658cf82c540d986b118f74f0fe1b2}

Deux nombres entiers, 0 ou plus, séparés par une virgule. Largeur et hauteur en pixels. L’une ou l’autre des valeurs peut être définie sur 0 pour ne pas être contrainte.

Ne s’applique pas aux requêtes imbriquées/incorporées.

## Par défaut {#section-b7338b2bf5114fff83b0714a57b20639}

Hérité de `default::DefaultPix` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
