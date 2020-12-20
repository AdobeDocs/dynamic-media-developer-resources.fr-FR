---
description: Sélecteur de mappage d’éclairage. Permet la sélection explicite de la carte d'éclairage à utiliser lors du rendu de ce matériau.
seo-description: Sélecteur de mappage d’éclairage. Permet la sélection explicite de la carte d'éclairage à utiliser lors du rendu de ce matériau.
seo-title: Illum
solution: Experience Manager
title: Illum
topic: Scene7 Image Serving - Image Rendering API
uuid: 2df0abbb-0d54-41b7-80c4-b914c18cd1b1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 3%

---


# Illum{#illum}

Sélecteur de mappage d’éclairage. Permet la sélection explicite de la carte d&#39;éclairage à utiliser lors du rendu de ce matériau.

## Propriétés {#section-162bcf562ca844ccba9e81e267508cca}

Enum. Définissez cette variable sur -1 pour la sélection automatique de la carte d’éclairage en fonction de la valeur de catalog::Gloss.

Définissez cette variable sur 0, 1 ou 2 pour sélectionner la carte d’éclairage A, B ou C. Le rendu choisira la carte d’éclairage la plus proche disponible dans la vignette.

## Par défaut {#section-ac386d31ef90423b8a367010a60bddc7}

-1 (sélection automatique)

## Voir aussi {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribut ::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)
