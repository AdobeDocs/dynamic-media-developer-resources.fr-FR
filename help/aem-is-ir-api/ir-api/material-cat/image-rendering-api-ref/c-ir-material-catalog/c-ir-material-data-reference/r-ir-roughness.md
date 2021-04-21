---
description: La rugosité de surface. Indique la brillance relative de la surface du matériau. Utilisé en association avec le type de catalogue et la brillance du catalogue pour contrôler les effets de rendu de la réflexion 3D.
solution: Experience Manager
title: Rogosité
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# Robustesse{#roughness}

La rugosité de surface. Indique la brillance relative de la surface du matériau. Utilisé conjointement avec catalog::Type et catalog::Gloss pour contrôler les effets de rendu de la réflexion 3D.

## Propriétés {#section-70c3f2394fd8477ca83a369448907971}

Nombre entier. Pourcentage dans la plage 0...100. Facultatif pour tous les matériaux. Utilisé uniquement pour les vignettes avec plusieurs plans de réflexion ou les vignettes avec la fonction de réflexion 3D. Laissez vide ou définissez -1 si vous n’êtes pas connu ou si vous n’en avez pas besoin.

## Par défaut {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; un serveur par défaut est utilisé.

## Voir aussi {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rugueuse=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ,  [catalogue::Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalogue::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
