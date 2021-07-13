---
description: Sélecteur de carte d’éclairage. Spécifie la carte d’éclairage avec laquelle ce matériau préfère être rendu.
solution: Experience Manager
title: illum
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---

# illum{#illum}

Sélecteur de carte d’éclairage. Spécifie la carte d’éclairage avec laquelle ce matériau préfère être rendu.

`illum=-1|0|1|2`

Si la carte d’éclairage spécifiée n’est pas disponible dans la vignette cible, la carte disponible la plus proche est utilisée à la place.

`illum=-1` indique que la carte d’éclairage est sélectionnée automatiquement en fonction de la  `gloss=` valeur.

## Propriétés {#section-aace8466566e4cf1a0c5a6c0167245c9}

Attribut de matière. Ignoré si la vignette ne définit pas plusieurs cartes d’éclairage.

## Par défaut {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Voir aussi {#section-9132e60381c64aa3a8ed1319690db55e}

[gsum=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
