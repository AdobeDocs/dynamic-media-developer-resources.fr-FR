---
title: IccRenderIntent
description: intention de rendu de conversion de couleurs. Il fournit l’intention de rendu par défaut pour les conversions de couleurs lorsque l’intention de rendu n’est pas spécifiée avec 'icc='.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

intention de rendu de conversion de couleurs. Fournit le mode de rendu par défaut pour les conversions de couleurs lorsque l’intention de rendu n’est pas spécifiée avec `icc=`.

## Propriétés {#section-0a38c60e1525426185616c42824aee2c}

Enum. Défini sur 0 pour la perception, 1 pour la colorimétrie relative, 2 pour la saturation, 3 pour la colorimétrie absolue. Laissez vide ou défini sur toute autre valeur afin de pouvoir utiliser l’intention de rendu par défaut définie dans le profil de couleurs.

## Par défaut {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Hérité de `default::IccRenderIntent`si non défini. Si elle est vide, l’expression « colorimétrie relative » est appliquée.

## Voir aussi {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute ::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute ::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
