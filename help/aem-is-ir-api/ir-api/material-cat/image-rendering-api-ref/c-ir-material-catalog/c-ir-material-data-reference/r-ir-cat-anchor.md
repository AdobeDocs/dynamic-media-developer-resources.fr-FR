---
description: Ancre d’image. Indique le point d’ancrage (zone réactive) d’une texture, d’une bordure du mur ou d’une image de décal répétable.
solution: Experience Manager
title: Ancre
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 3%

---


# Ancre{#anchor}

Ancre d’image. Indique le point d’ancrage (zone réactive) d’une texture, d’une bordure du mur ou d’une image de décal répétable.

Une texture répétable est appliquée à un objet de vignette de sorte que le point d’ancrage de la texture se trouve au point d’origine de la texture de l’objet. Une image de poubelle est appliquée à un objet de vignette de sorte que le point d’ancrage de la poubelle se trouve au point d’origine de la poubelle de l’objet. Pour les bordures murales, seule la valeur x est utilisée ; la valeur y est ignorée.

## Propriétés {#section-bc4bc8b897c64535b88681e57d72942f}

Deux nombres entiers, séparés par une virgule. Décalage des pixels par rapport au coin supérieur gauche de l’image. Ignoré si `catalog::Alignment=3` et par couleur unie et matériaux de l&#39;armoire.

## Par défaut {#section-b7ccc419a356415294706cd295ae96c9}

Si le champ est vide ou non présent, le coin supérieur gauche (0,0) de l&#39;image pour les matériaux de texture répétables est utilisé, ou le centre de l&#39;image en cas de matériaux décaux.

## Voir aussi {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catalogue : Alignement](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [ancrage=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
