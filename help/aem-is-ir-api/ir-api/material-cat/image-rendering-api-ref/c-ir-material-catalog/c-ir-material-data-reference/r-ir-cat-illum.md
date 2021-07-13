---
description: Sélecteur de carte d’éclairage. Permet une sélection explicite de la carte d'éclairage à utiliser lors du rendu de ce matériau.
solution: Experience Manager
title: Illum
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 5e74b3e8-6289-4114-aa11-a6f91671363e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 4%

---

# Illum{#illum}

Sélecteur de carte d’éclairage. Permet une sélection explicite de la carte d&#39;éclairage à utiliser lors du rendu de ce matériau.

## Propriétés {#section-162bcf562ca844ccba9e81e267508cca}

Enum. Définissez cette variable sur -1 pour la sélection automatique de la carte d’éclairage en fonction de la valeur de catalog::Glessure.

Définissez cette variable sur 0, 1 ou 2 pour sélectionner les cartes d’éclairage A, B ou C. Le moteur de rendu choisira la carte d’éclairage la plus proche disponible dans la vignette.

## Par défaut {#section-ac386d31ef90423b8a367010a60bddc7}

-1 (sélection automatique)

## Voir aussi {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribute::Glessé](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)
