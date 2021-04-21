---
description: Taille de miniature par défaut. Utilisé à la place de l’attribut DefaultPix pour les requêtes de miniature (req=tmb).
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# DefaultThumbPix{#defaultthumbpix}

Taille de miniature par défaut. Utilisé à la place d’attribut::DefaultPix pour les requêtes de miniature (req=tmb).

Le serveur limite la largeur et la hauteur des images de réponse si une requête de miniature ( `req=tmb`) ne spécifie pas explicitement la taille de la vue en utilisant explicitement `wid=`, `hei=` ou `scl=`.

## Propriétés {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Deux nombres entiers, 0 ou plus, séparés par une virgule. Largeur et hauteur en pixels. L’une ou l’autre des valeurs peut être définie sur 0 pour ne pas être contrainte.

Ne s’applique pas aux requêtes imbriquées/incorporées.

## Par défaut {#section-2c4a4f14540449638822913513170ff1}

Hérité de `default::DefaultThumbPix` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [attribut::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
