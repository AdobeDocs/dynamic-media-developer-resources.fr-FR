---
title: Illum
description: Sélecteur de carte d’éclairage. Il permet une sélection explicite de la carte d’éclairage à utiliser lors du rendu de ce matériau.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e74b3e8-6289-4114-aa11-a6f91671363e
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 3%

---

# Illum{#illum}

Sélecteur de carte d’éclairage. Il permet une sélection explicite de la carte d’éclairage à utiliser lors du rendu de ce matériau.

## Propriétés {#section-162bcf562ca844ccba9e81e267508cca}

Enum. Définissez cette variable sur -1 pour la sélection automatique de la carte d’éclairage en fonction de la valeur de catalog::Glessure.

Définissez cette variable sur 0, 1 ou 2 pour sélectionner la carte d’éclairage A, B ou C. Le moteur de rendu choisit la carte d’éclairage la plus proche disponible dans la vignette.

## Par défaut {#section-ac386d31ef90423b8a367010a60bddc7}

-1 (sélection automatique)

## Voir aussi {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribute::Glessé](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)
