---
description: Sélecteur de filigrane. Indique l’ID de catalogue de l’enregistrement de catalogue à utiliser comme image ou modèle de filigrane.
solution: Experience Manager
title: Filigrane
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# Filigrane{#watermark}

Sélecteur de filigrane. Spécifie le catalogue : : ID de l’enregistrement de catalogue à utiliser comme image ou modèle de filigrane.

Si spécifié, le serveur applique le filigrane aux données image demandées pour toutes les demandes d’image ( `req=img`).

## Propriétés {#section-fad6ffff4c5f4b5c8010281bc1377055}

Chaîne de texte. Si spécifié, doit être une valeur `Catalog::Id` valide dans ce catalogue d’images (ou dans le catalogue par défaut, s’il est spécifié dans [!DNL default.ini]).

## Par défaut {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Hérité de `default::Watermark` si elle n’est pas définie. S’il est défini, mais vide, aucun filigrane n’est appliqué pour ce catalogue d’images, même si `default::Watermark` est défini.

## Voir aussi {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
