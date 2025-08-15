---
description: Élément de filtre d’adresse. Facultatif dans les éléments <rule>. Il remplace l’attribut ClientAddressFilter lorsque la règle est appliquée.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---

# addressfilter{#addressfilter}

Élément de filtre d’adresse. Facultatif dans les éléments `<rule>`. Il remplace attribute::ClientAddressFilter lorsque la règle est appliquée.

## Attributs {#section-e7a0960f7f0045da91de37824aa4aeaa}

Aucune

## Données {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Liste d’adresses IP séparées par des virgules. Chaque adresse individuelle peut inclure un suffixe de masque de réseau facultatif pour permettre la spécification de plages d&#39;adresses IP. Voir [attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) pour plus de détails.

## Description {#section-099b7839c4be40c68cbff29dad14e7d5}

L’accès à ce catalogue d’images peut être limité à une ou plusieurs adresses IP spécifiques en les spécifiant dans un élément `<addressfilter>`. Une erreur de type « demande refusée » est renvoyée au client si l’adresse IP du client ne correspond pas.

L’accès n’est pas limité si `<addressfilter>` est vide ou non spécifié.

Si la `<expression>` dans l’élément `<rule>` est absente ou vide, la `<addressfilter>` est appliquée à toutes les requêtes.

`localhost` fait toujours implicitement partie de la définition du `ClientAddressFilter`, même si elle n’est pas explicitement spécifiée. Les requêtes provenant de `localhost` ne sont jamais rejetées, quelle que soit la spécification `ClientAddressFilter`.

## Voir aussi {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
