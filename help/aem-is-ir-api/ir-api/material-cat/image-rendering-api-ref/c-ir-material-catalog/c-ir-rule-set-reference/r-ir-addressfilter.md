---
description: Élément filtre d’adresse. Facultatif dans les éléments <rule>. Remplace l’attribut ClientAddressFilter lorsque la règle est appliquée.
seo-description: Élément filtre d’adresse. Facultatif dans les éléments <rule>. Remplace l’attribut ClientAddressFilter lorsque la règle est appliquée.
seo-title: adressfilter
solution: Experience Manager
title: adressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# adressfilter{#addressfilter}

Élément filtre d’adresse. Facultatif dans `<rule>` les éléments. Remplace l’attribut ::ClientAddressFilter lorsque la règle est appliquée.

## Attributes {#section-e7a0960f7f0045da91de37824aa4aeaa}

Aucune

## Données {#section-eb138f192516418a9ef2ab9a38c9ee9e}

d’adresses IP séparé par des virgules. Chaque adresse individuelle peut inclure un suffixe de masque de réseau facultatif afin de permettre la spécification des plages d&#39;adresses IP. See ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` for details.

## Description {#section-099b7839c4be40c68cbff29dad14e7d5}

L’accès à ce catalogue d’images peut être limité à une ou plusieurs adresses IP spécifiques en les spécifiant dans un `<addressfilter>` élément. Une erreur &quot;demande refusée&quot; est renvoyée au client si l’adresse IP du client ne correspond pas.

L’accès n’est pas restreint si `<addressfilter>` il est vide ou non spécifié.

Si le `<expression>` contenu de l’ `<rule>` élément est absent ou vide, le `<addressfilter>` paramètre est appliqué à toutes les requêtes.

`localhost` fait toujours implicitement partie de la `ClientAddressFilter` définition, même si elle n’est pas explicitement spécifiée. Les demandes provenant de `localhost` ne sont jamais rejetées, quelle que soit la `ClientAddressFilter` spécification.

## Voir aussi {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribut::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
