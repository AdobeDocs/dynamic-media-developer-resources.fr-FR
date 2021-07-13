---
description: La rugosité de surface. Indique la brillance relative de la surface du matériau. Utilisé conjointement avec le type de catalogue et le brillant de catalogue pour contrôler les effets de rendu de reflet 3D.
solution: Experience Manager
title: Rogosité
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# Rogosité{#roughness}

La rugosité de surface. Indique la brillance relative de la surface du matériau. Utilisé conjointement avec catalog::Type et catalog::Glessor pour contrôler les effets de rendu de la réflexion 3D.

## Propriétés {#section-70c3f2394fd8477ca83a369448907971}

Nombre entier. Valeur en pourcentage comprise entre 0 et 100. Facultatif pour tous les matériaux. Utilisé uniquement pour les vignettes avec plusieurs plans de réflexion ou les vignettes avec des fonctions de réflexion 3D. Laissez vide ou définissez sur -1 si vous n’êtes pas connu ou si vous n’êtes pas nécessaire.

## Par défaut {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; une valeur par défaut du serveur est utilisée.

## Voir aussi {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rugir=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ,  [catalogue::Glessure](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalogue::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
