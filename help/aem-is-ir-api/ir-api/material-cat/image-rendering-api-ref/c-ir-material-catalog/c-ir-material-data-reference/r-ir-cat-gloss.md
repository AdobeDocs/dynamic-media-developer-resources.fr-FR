---
description: Lissage de surface Indique la brillance relative de la surface du matériau.
seo-description: Lissage de surface Indique la brillance relative de la surface du matériau.
seo-title: Éclat
solution: Experience Manager
title: Éclat
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Éclat{#gloss}

Lissage de surface Indique la brillance relative de la surface du matériau.

Cette valeur est utilisée par le rendu aux fins suivantes :

* Sélectionnez la carte d’éclairage lorsque `catalog::Illum` la valeur est -1.
* Contrôle le rendu de l’effet d’éclat (réflexion spéculaire) conjointement avec `catalog::Type`.
* Contrôle les effets de rendu du reflet 3D conjointement avec `catalog::Type` et `catalog::Roughness`.

## Propriétés {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Nombre entier. Pourcentage dans la plage 0...100. Facultatif pour tous les matériaux. Utilisé uniquement pour les vignettes avec plusieurs cartes de réflexion ou les vignettes avec la fonction de réflexion 3D. Laissez vide ou défini sur -1 s’il n’est pas connu ou s’il n’est pas nécessaire.

## Par défaut {#section-2352721073524f1a8d461f64a363aac9}

Une valeur par défaut est fournie par la vignette si cette valeur est définie sur -1.

## Voir aussi {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
