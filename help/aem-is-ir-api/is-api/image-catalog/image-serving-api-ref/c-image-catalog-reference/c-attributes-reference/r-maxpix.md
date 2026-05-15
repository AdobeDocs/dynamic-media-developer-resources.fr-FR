---
description: Limite de taille des images de réponse. Largeur et hauteur maximales de l’image de réponse pouvant être renvoyées au client.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
TQID: 'https://experienceleague.adobe.com/lX4ooC7B0VIJDRr0yZJVmp45qnXbSuimMZSyU9rWLcw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 3%

---

# MaxPix{#maxpix}

Limite de taille des images de réponse. Largeur et hauteur maximales de l’image de réponse pouvant être renvoyées au client.

Le serveur renvoie une erreur si une requête provoquait une image de réponse dont la largeur ou la hauteur est supérieure à `attribute::MaxPix`.

## Propriétés {#section-b175425b9e9f48e0b1a71640f6a9e936}

Deux nombres entiers supérieurs à 0 séparés par une virgule. Largeur et hauteur en pixels. Peut également être défini sur `0,0` pour permettre toute taille d’image de réponse sans limite.

## Par défaut {#section-1003537434da432fb2af100ecdbf9d72}

Hérité de `default::MaxPix` si non défini ou si vide.

## Voir aussi {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
