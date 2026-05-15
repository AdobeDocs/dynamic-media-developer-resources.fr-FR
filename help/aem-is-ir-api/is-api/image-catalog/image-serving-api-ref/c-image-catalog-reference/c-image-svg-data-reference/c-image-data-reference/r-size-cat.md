---
description: Taille de l’image. Taille en pixels de l’image en pleine résolution référencée par le chemin d’accès au catalogue.
solution: Experience Manager
title: Taille
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
TQID: 'https://experienceleague.adobe.com/wS28XEIvINBBoYZSI-frpSbCikCyC5AhT6TyDgMsGFg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 5%

---

# Taille{#size}

Taille de l’image. Taille en pixels de l’image pleine résolution référencée par catalog::Path.

Si cette valeur est fournie, le service d’images l’utilise pour éviter d’avoir à ouvrir l’image pour obtenir la taille réelle de l’image.

>[!NOTE]
>
>Si `catalog::Size` est fourni et n’est pas identique à la taille réelle de l’image en pleine résolution, un comportement indéfini peut s’ensuivre.

## Propriétés {#section-5c914ec8b1444a8e99d811b647cd42a3}

Deux nombres entiers, chacun supérieur à 0, séparés par une virgule. Facultatif.

## Par défaut {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Si le champ n’est pas présent ou s’il est vide, la taille réelle de l’image est utilisée.

## Voir aussi {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
