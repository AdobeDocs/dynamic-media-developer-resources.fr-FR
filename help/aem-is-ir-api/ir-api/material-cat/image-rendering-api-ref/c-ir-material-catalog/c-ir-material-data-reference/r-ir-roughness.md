---
description: Rugosité de surface. Indique la brillance relative de la surface du matériau. Utilisé conjointement avec Type de catalogue et Gloss de catalogue pour contrôler les effets de rendu de réflexion 3D.
solution: Experience Manager
title: Rugosité
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 2%

---

# Rugosité{#roughness}

Rugosité de surface. Indique la brillance relative de la surface du matériau. Utilisé conjointement avec catalog::Type et catalog::Gloss pour contrôler les effets de rendu de réflexion 3D.

## Propriétés {#section-70c3f2394fd8477ca83a369448907971}

Nombre entier. Valeur de pourcentage comprise entre 0 et 100. Facultatif pour tous les matériaux. Utilisé uniquement pour les vignettes avec plusieurs cartes de réflexion ou les vignettes avec fonction de réflexion 3D. Laissez vide ou définissez sur -1 si vous ne le savez pas ou si vous n’en avez pas besoin.

## Par défaut {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1 ; une valeur serveur par défaut est utilisée.

## Voir aussi {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[raw=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catalog::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
