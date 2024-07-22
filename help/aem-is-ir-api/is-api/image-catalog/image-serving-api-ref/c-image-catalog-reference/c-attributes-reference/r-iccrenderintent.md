---
title: IccRenderIntent
description: Mode de rendu de conversion des couleurs. Elle fournit l’intention de rendu par défaut pour les conversions de couleurs lorsque "icc=" n’est pas spécifié pour l’intention de rendu.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 3%

---

# IccRenderIntent{#iccrenderintent}

Mode de rendu de conversion des couleurs. Fournit l’intention de rendu par défaut pour les conversions de couleurs lorsque l’intention de rendu n’est pas spécifiée avec `icc=`.

## Propriétés {#section-2540099fb2fc47d29b04642da4f5922a}

Enum. Définissez cette valeur sur 0 pour la perception, 1 pour la colorimétrie relative, 2 pour la saturation et 3 pour la colorimétrie absolue.

## Par défaut {#section-61a05067905b44099c228e15de279dbd}

Hérité de `default::IccRenderIntent` si elle n’est pas définie ou si elle est vide.

## Voir aussi {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
