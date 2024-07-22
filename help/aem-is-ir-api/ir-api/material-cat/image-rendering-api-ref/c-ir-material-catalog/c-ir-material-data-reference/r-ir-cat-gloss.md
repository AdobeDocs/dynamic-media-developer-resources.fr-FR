---
description: Luminosité de surface Indique la brillance relative de la surface du matériau.
solution: Experience Manager
title: Grain
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 2%

---

# Grain{#gloss}

Luminosité de surface Indique la brillance relative de la surface du matériau.

Cette valeur est utilisée par le moteur de rendu aux fins suivantes :

* Sélectionnez la carte d’éclairage lorsque `catalog::Illum` est -1.
* Contrôle le rendu de l’effet de brillance (réflexion spéculaire) conjointement avec `catalog::Type`.
* Contrôle les effets de rendu de la réflexion 3D conjointement avec `catalog::Type` et `catalog::Roughness`.

## Propriétés {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Nombre entier. Nombre en pourcentage dans la plage 0...100. Facultatif pour tous les matériaux. Utilisé uniquement pour les vignettes avec plusieurs plans de réflexion ou les vignettes avec des fonctions de réflexion 3D. Laissez vide ou définissez sur -1 si vous n’êtes pas connu ou si vous n’êtes pas nécessaire.

## Par défaut {#section-2352721073524f1a8d461f64a363aac9}

Une valeur par défaut est fournie par la vignette si cette valeur est définie sur -1.

## Voir aussi {#section-0213bbdb7d6d4974a7c53822957717c1}

[gless=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog::Roghness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
