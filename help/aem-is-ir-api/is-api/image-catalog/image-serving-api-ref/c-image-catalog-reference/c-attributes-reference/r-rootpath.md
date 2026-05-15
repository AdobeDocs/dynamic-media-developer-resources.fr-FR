---
description: Chemin d’accès racine des données Source. Chemin d’accès absolu ou relatif au dossier racine pour les données sources de ce catalogue d’images.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
TQID: 'https://experienceleague.adobe.com/WFDqweSZS1tNJppprC8pJblN-7LBKRM-IHt2Vfj3oW0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 111
ht-degree: 2%

---

# RootPath{#rootpath}

Chemin d’accès racine des données Source. Chemin d’accès absolu ou relatif au dossier racine pour les données sources de ce catalogue d’images.

La `RootPath` est une valeur de chaîne de texte. Voir [&#x200B; Gestion des données Source](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) pour plus d’informations sur les chemins d’accès racine au serveur.

## Propriétés {#section-b41d7e0ea63143eb8034569706cad0c0}

Chaîne de texte. Doit être vide, un chemin d’accès relatif valide au dossier ou un chemin d’accès absolu valide accessible par le serveur d’images.

## Par défaut {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Hérité de `default::RootPath` si non défini. S’il est défini mais vide, il ne contribue pas au chemin d’accès racine du fichier source.

## Voir aussi {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Gestion des données Source](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
