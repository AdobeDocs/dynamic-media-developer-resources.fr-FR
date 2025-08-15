---
description: Résolution de miniature par défaut. Fournit une valeur par défaut pour la résolution de l’objet de miniature au cas où un enregistrement de catalogue particulier ne contiendrait pas de valeur ThumbRes de catalogue valide.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0abb680e-8944-4ad8-9b6c-d0a7559fdd1b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 3%

---

# ThumbRes{#thumbres}

Résolution de miniature par défaut. Fournit une valeur par défaut pour la résolution de l’objet de miniature au cas où un enregistrement de catalogue particulier ne contiendrait pas de valeur catalog::ThumbRes valide.

Utilisé uniquement pour les requêtes de miniature ( `req=tmb`) et lorsqu’il est `catalog::ThumbType=3`.

## Propriétés {#section-88d37d0e030f4879a9e584dd2cc780f3}

Nombre réel, supérieur à 0. Généralement exprimé en pixels par pouce, mais peut également être exprimé dans d’autres unités, comme les pixels par mètre.

## Par défaut {#section-86588899ec9b4276a98b03d7faf64003}

Hérité de `default::ThumbRes` si non défini ou si vide.

## Voir aussi {#section-a6d2cce2e404441a996dba98a95c8e16}

[catalog::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
