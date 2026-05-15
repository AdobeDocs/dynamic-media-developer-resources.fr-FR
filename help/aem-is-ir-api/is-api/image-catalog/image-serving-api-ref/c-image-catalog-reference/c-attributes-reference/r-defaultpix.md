---
description: Taille d’affichage par défaut.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
TQID: 'https://experienceleague.adobe.com/R8zszzJJqviiIiIBt4GHGUmg5cX1yDxuhT6zoHllQKw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# DefaultPix{#defaultpix}

Taille d’affichage par défaut.

Le serveur oblige les images de réponse à ne pas dépasser ces valeurs de largeur et de hauteur, si la requête ne spécifie pas explicitement la taille d’affichage à l’aide de `wid=`, `hei=` ou `scl=`.

## Propriétés {#section-c3e658cf82c540d986b118f74f0fe1b2}

Deux nombres entiers, supérieurs ou égaux à zéro, séparés par une virgule. Largeur et hauteur en pixels. Vous pouvez définir les deux valeurs sur 0 pour qu’elles ne soient pas contraintes.

Ne s’applique pas aux requêtes imbriquées/incorporées.

## Par défaut {#section-b7338b2bf5114fff83b0714a57b20639}

Hérité de `default::DefaultPix` si non défini ou si vide.

## Voir aussi {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [catalog::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
