---
title: IccRenderIntent
description: Mode de rendu de conversion des couleurs. Fournit l’intention de rendu par défaut pour les conversions de couleurs lorsque l’intention de rendu n’est pas spécifiée par icc=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---

# IccRenderIntent{#iccrenderintent}

Mode de rendu de conversion des couleurs. Fournit l’intention de rendu par défaut pour les conversions de couleurs lorsque l’intention de rendu n’est pas spécifiée avec `icc=`.

## Propriétés {#section-0a38c60e1525426185616c42824aee2c}

Enum. Définissez cette valeur sur 0 pour la perception, 1 pour la colorimétrie relative, 2 pour la saturation et 3 pour la colorimétrie absolue. Conservez vide ou définissez sur une autre valeur pour utiliser l’intention de rendu par défaut définie dans le profil colorimétrique.

## Par défaut {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Hérité de `default::IccRenderIntent`si elle n’est pas définie. S’il est vide, la &quot;colorimétrie relative&quot; est appliquée.

## Voir aussi {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
