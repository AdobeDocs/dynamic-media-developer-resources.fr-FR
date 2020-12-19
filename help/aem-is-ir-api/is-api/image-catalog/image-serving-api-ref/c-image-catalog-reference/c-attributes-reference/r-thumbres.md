---
description: Résolution de miniature par défaut. Fournit une valeur par défaut pour la résolution d’objet de miniature au cas où un enregistrement de catalogue spécifique ne contiendrait pas de valeur ThumbRes de catalogue valide.
seo-description: Résolution de miniature par défaut. Fournit une valeur par défaut pour la résolution d’objet de miniature au cas où un enregistrement de catalogue spécifique ne contiendrait pas de valeur ThumbRes de catalogue valide.
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Scene7 Image Serving - Image Rendering API
uuid: 4a77d673-9d2e-4e62-a014-c99fa3df294a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# ThumbRes{#thumbres}

Résolution de miniature par défaut. Fournit une valeur par défaut pour la résolution d’objet de miniature au cas où un enregistrement de catalogue spécifique ne contiendrait pas une valeur catalog::ThumbRes valide.

Utilisé uniquement pour les requêtes miniatures ( `req=tmb`) et lorsque `catalog::ThumbType=3`.

## Propriétés {#section-88d37d0e030f4879a9e584dd2cc780f3}

Nombre réel, supérieur à 0.Généralement exprimé en pixels par pouce, mais peut également se trouver dans d’autres unités, telles que les pixels par mètre.

## Par défaut {#section-86588899ec9b4276a98b03d7faf64003}

Hérité de `default::ThumbRes` si elle n&#39;est pas définie ou si elle est vide.

## Voir aussi {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalogue ::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
