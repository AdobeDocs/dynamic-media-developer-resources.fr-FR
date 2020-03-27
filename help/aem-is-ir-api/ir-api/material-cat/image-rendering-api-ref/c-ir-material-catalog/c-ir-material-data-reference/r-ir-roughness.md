---
description: Rogosité de surface. Indique la brillance relative de la surface du matériau. Utilisé en association avec le type de catalogue et l’éclat du catalogue pour contrôler les effets de rendu de reflet 3D.
seo-description: Rogosité de surface. Indique la brillance relative de la surface du matériau. Utilisé en association avec le type de catalogue et l’éclat du catalogue pour contrôler les effets de rendu de reflet 3D.
seo-title: Rogosité
solution: Experience Manager
title: Rogosité
topic: Scene7 Image Serving - Image Rendering API
uuid: d71e4411-dd59-4347-a7c2-132e130ff36b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Rogosité{#roughness}

Rogosité de surface. Indique la brillance relative de la surface du matériau. Utilisé conjointement avec catalog::Type et catalog::Gloss pour contrôler les effets de rendu de reflet 3D.

## Propriétés {#section-70c3f2394fd8477ca83a369448907971}

Nombre entier. Pourcentage dans la plage 0...100. Facultatif pour tous les matériaux. Utilisé uniquement pour les vignettes avec plusieurs cartes de réflexion ou les vignettes avec la fonction de réflexion 3D. Laissez vide ou défini sur -1 s’il n’est pas connu ou s’il n’est pas nécessaire.

## Par défaut {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; une valeur par défaut du serveur est utilisée.

## Voir aussi {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
