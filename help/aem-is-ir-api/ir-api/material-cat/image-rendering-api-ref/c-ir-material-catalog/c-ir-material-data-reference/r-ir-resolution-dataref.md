---
description: Résolution. Résolution d’image "du monde réel", généralement exprimée en pixels par pouce, mais peut également se trouver dans d’autres unités, telles que les pixels par mètre.
solution: Experience Manager
title: Résolution
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# Résolution{#resolution}

Résolution. Résolution d’image &quot;du monde réel&quot;, généralement exprimée en pixels par pouce, mais peut également se trouver dans d’autres unités, telles que les pixels par mètre.

## Propriétés {#section-985ca2ad858c4e9c9cbb303f55447553}

Nombre réel, supérieur à 0. Requis pour les matériaux de texture et de décal, sauf si la résolution de l’image est identique à l’attribut::Resolution. Ignoré par les matériaux de couleur et d’armoire solides.

## Par défaut {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` est utilisé si le champ n’est pas présent, si la valeur est 0 ou négative, ou si le champ est vide.

## Voir aussi {#section-2d04df523d7345f6929178cbc637da78}

[attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) ,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
