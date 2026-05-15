---
description: Ancre d’image. Indique le point d’ancrage (zone réactive) d’une texture répétable, d’une bordure de mur ou d’une image de vignette.
solution: Experience Manager
title: Ancre
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
TQID: 'https://experienceleague.adobe.com/-TWQdh61Hkdr81vXooodDafEwQHTMvQdSQSf--HuPIg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 3%

---

# Ancre{#anchor}

Ancre d’image. Indique le point d’ancrage (zone réactive) d’une texture répétable, d’une bordure de mur ou d’une image de vignette.

Une texture répétable est appliquée à un objet vignette de sorte que le point d&#39;ancrage de texture soit situé au point d&#39;origine de texture de l&#39;objet. Une image de vignette est appliquée à un objet vignette de sorte que le point d&#39;ancrage de vignette se trouve au point d&#39;origine de la vignette de l&#39;objet. Pour les bordures de mur, seule la valeur x est utilisée ; la valeur y est ignorée.

## Propriétés {#section-bc4bc8b897c64535b88681e57d72942f}

Deux nombres entiers séparés par une virgule. Décalage en pixels par rapport au coin supérieur gauche de l’image. Ignoré si `catalog::Alignment=3` et par la couleur unie et les matériaux de l&#39;armoire.

## Par défaut {#section-b7ccc419a356415294706cd295ae96c9}

Si le champ est vide ou absent, le coin supérieur gauche (0,0) de l&#39;image pour les matériaux de texture répétables est utilisé, ou le centre de l&#39;image dans le cas des matériaux de vignette.

## Voir aussi {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
