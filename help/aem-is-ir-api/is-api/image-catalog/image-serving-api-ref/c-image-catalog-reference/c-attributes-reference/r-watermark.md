---
description: Sélecteur de filigrane. Indique l’ID de catalogue de l’enregistrement de catalogue à utiliser comme image ou modèle de filigrane.
solution: Experience Manager
title: Filigrane
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 5%

---


# Filigrane{#watermark}

Sélecteur de filigrane. Indique le catalogue ::Id de l’enregistrement de catalogue à utiliser comme image ou modèle de filigrane.

Si spécifié, le serveur applique le filigrane aux données d’image demandées pour toutes les demandes d’image ( `req=img`).

## Propriétés {#section-fad6ffff4c5f4b5c8010281bc1377055}

Chaîne de texte. Si spécifié, doit être une valeur `Catalog::Id` valide dans ce catalogue d’images (ou dans le catalogue par défaut, si spécifiée dans [!DNL default.ini]).

## Par défaut {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Hérité de `default::Watermark` si elle n&#39;est pas définie. Si elle est définie mais vide, aucun filigrane n’est appliqué à ce catalogue d’images, même si `default::Watermark` est défini.

## Voir aussi {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
