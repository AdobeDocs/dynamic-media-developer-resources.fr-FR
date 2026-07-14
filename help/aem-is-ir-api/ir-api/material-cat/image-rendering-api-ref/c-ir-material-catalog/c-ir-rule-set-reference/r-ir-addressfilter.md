---
description: Élément de filtre d’adresse. Facultatif dans les éléments <rule>. Il remplace l’attribut ClientAddressFilter lorsque la règle est appliquée.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
TQID: 'https://experienceleague.adobe.com/583zFF80AMZnaF4C-RQpRQI684hRlPRCuwoMPHGJ6eg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 150
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

