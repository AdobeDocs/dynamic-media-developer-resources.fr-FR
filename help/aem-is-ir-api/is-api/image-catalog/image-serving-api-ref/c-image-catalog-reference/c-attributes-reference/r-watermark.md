---
description: Sélecteur de filigrane. Indique l’ID catalogue de l’enregistrement de catalogue à utiliser comme image ou modèle de filigrane.
solution: Experience Manager
title: Filigrane
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
TQID: 'https://experienceleague.adobe.com/zajYc7BBw0BfJ6qvnTFiHY79quRa91-LdY3j1YynxVc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 2%

---

# Filigrane{#watermark}

Sélecteur de filigrane. Indique le catalog::Id de l’enregistrement de catalogue à utiliser comme image ou modèle de filigrane.

S’il est spécifié, le serveur applique le filigrane aux données d’image demandées pour toutes les demandes d’image ( `req=img`).

## Propriétés {#section-fad6ffff4c5f4b5c8010281bc1377055}

Chaîne de texte. Si elle est spécifiée, doit être une valeur de `Catalog::Id` valide dans ce catalogue d’images (ou dans le catalogue par défaut, si spécifié dans [!DNL default.ini]).

## Par défaut {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Hérité de `default::Watermark` si non défini. Si défini mais vide, aucun filigrane n’est appliqué pour ce catalogue d’images, même si `default::Watermark` est défini.

## Voir aussi {#section-f15dbe31013849828d78588742dde58e}

[catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
