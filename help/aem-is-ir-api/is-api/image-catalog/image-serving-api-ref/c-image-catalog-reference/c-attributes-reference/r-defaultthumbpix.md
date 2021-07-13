---
description: Taille de miniature par défaut. Utilisé à la place de l’attribut DefaultPix pour les demandes de miniature (req=tmb).
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# DefaultThumbPix{#defaultthumbpix}

Taille de miniature par défaut. Utilisé à la place d’attribute::DefaultPix pour les demandes de miniature (req=tmb).

Le serveur oblige les images de réponse à ne pas dépasser cette largeur et cette hauteur, si une demande de miniature ( `req=tmb`) ne spécifie pas explicitement la taille d’affichage en utilisant `wid=`, `hei=` ou `scl=`.

## Propriétés {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Deux nombres entiers, 0 ou plus, séparés par une virgule. Largeur et hauteur en pixels. L’une ou l’autre des valeurs (ou les deux) peuvent être définies sur 0 pour ne pas être contraintes.

Ne s’applique pas aux requêtes imbriquées/incorporées.

## Par défaut {#section-2c4a4f14540449638822913513170ff1}

Hérité de `default::DefaultThumbPix` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
