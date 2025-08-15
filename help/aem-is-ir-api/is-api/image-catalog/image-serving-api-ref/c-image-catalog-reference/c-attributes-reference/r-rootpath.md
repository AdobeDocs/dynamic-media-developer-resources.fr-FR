---
description: Chemin racine des données source. Chemin d’accès absolu ou relatif du dossier racine pour les données source de ce catalogue d’images.
solution: Experience Manager
title: Chemin racine
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# Chemin racine{#rootpath}

Chemin racine des données source. Chemin d’accès absolu ou relatif du dossier racine pour les données source de ce catalogue d’images.

La `RootPath` valeur est une valeur de chaîne de texte. Voir [Gestion des données](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) sources pour plus d’informations sur les chemins racine du serveur.

## Propriétés {#section-b41d7e0ea63143eb8034569706cad0c0}

Chaîne de texte. Doit être vide, un chemin d’accès au dossier relatif valide ou un chemin absolu valide accessible par le serveur d’images.

## Par défaut {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Hérité de `default::RootPath` si non défini. S’il est défini mais vide, il ne contribue pas au chemin racine du fichier source.

## Voir aussi {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog ::P ath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog ::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md),  [ruleset ::P athRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Gestion des données source](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
