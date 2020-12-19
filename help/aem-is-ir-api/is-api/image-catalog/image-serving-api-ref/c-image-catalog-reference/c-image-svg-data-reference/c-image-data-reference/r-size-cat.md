---
description: Taille de l’image. Taille en pixels de l’image en résolution totale référencée par le chemin d’accès au catalogue.
seo-description: Taille de l’image. Taille en pixels de l’image en résolution totale référencée par le chemin d’accès au catalogue.
seo-title: Taille
solution: Experience Manager
title: Taille
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 11%

---


# Taille{#size}

Taille de l’image. Taille en pixels de l’image en résolution totale référencée par catalog::Path.

Si cette valeur est fournie, la diffusion d’images l’utilise pour éviter d’avoir à ouvrir l’image pour obtenir la taille réelle de l’image.

>[!NOTE]
>
>Si `catalog::Size`est fourni et n’est pas identique à la taille réelle de l’image en pleine résolution, un comportement non défini peut en résulter.

## Propriétés {#section-5c914ec8b1444a8e99d811b647cd42a3}

Deux nombres entiers, chacun supérieur à 0, séparés par une virgule. Facultatif.

## Par défaut {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Si le champ n’est pas présent ou s’il est vide, la taille réelle de l’image est utilisée.

## Voir aussi {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalogue ::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
