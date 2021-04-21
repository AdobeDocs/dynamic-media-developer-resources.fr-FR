---
description: Taille limite de l’image de réponse. Largeur et hauteur maximales de l’image de réponse qui peuvent être renvoyées au client.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# MaxPix{#maxpix}

Taille limite de l’image de réponse. Largeur et hauteur maximales de l’image de réponse qui peuvent être renvoyées au client.

Le serveur renvoie une erreur si une requête provoque une image de réponse dont la largeur ou la hauteur est supérieure à `attribute::MaxPix`.

## Propriétés {#section-b175425b9e9f48e0b1a71640f6a9e936}

Deux nombres entiers, supérieurs à 0, séparés par une virgule. Largeur et hauteur en pixels. Peut également être défini sur `0,0` pour autoriser toute taille d’image de réponse sans limite.

## Par défaut {#section-1003537434da432fb2af100ecdbf9d72}

Hérité de `default::MaxPix` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
