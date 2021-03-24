---
description: Sélecteur de mappage d’éclairage. Indique la carte d’éclairage avec laquelle ce matériau préfère être rendu.
solution: Experience Manager
title: illum
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 4%

---


# illum{#illum}

Sélecteur de mappage d’éclairage. Indique la carte d’éclairage avec laquelle ce matériau préfère être rendu.

`illum=-1|0|1|2`

Si la carte d’éclairage spécifiée n’est pas disponible dans la vignette de cible, la carte disponible la plus proche est utilisée à la place.

`illum=-1` indique que la carte d’éclairage est sélectionnée automatiquement en fonction de la  `gloss=` valeur.

## Propriétés {#section-aace8466566e4cf1a0c5a6c0167245c9}

Attribut de matériau. Ignoré si la vignette ne définit pas plusieurs cartes d’éclairage.

## Par défaut {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Voir aussi {#section-9132e60381c64aa3a8ed1319690db55e}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
