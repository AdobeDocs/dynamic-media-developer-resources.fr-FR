---
description: Lissage de surface Indique la brillance relative de la surface du matériau.
solution: Experience Manager
title: Éclat
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# Gloss{#gloss}

Lissage de surface Indique la brillance relative de la surface du matériau.

Cette valeur est utilisée par le rendu aux fins suivantes :

* Sélectionnez la carte d&#39;éclairage lorsque `catalog::Illum` est -1.
* Contrôle le rendu de l’effet de brillance (réflexion spéculaire) conjointement avec `catalog::Type`.
* Contrôle les effets de rendu de la réflexion 3D conjointement avec `catalog::Type` et `catalog::Roughness`.

## Propriétés {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Nombre entier. Pourcentage dans la plage 0...100. Facultatif pour tous les matériaux. Utilisé uniquement pour les vignettes avec plusieurs plans de réflexion ou les vignettes avec la fonction de réflexion 3D. Laissez vide ou définissez -1 si vous n’êtes pas connu ou si vous n’en avez pas besoin.

## Par défaut {#section-2352721073524f1a8d461f64a363aac9}

La vignette fournit une valeur par défaut si elle est définie sur -1.

## Voir aussi {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [catalog::Roughness](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
