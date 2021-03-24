---
description: Élément de filtre d’adresses. Facultatif dans les éléments <rule>. Remplace l’attribut ClientAddressFilter lorsque la règle est appliquée.
solution: Experience Manager
title: adressfiltre
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 1%

---


# address filter{#addressfilter}

Élément de filtre d’adresses. Facultatif dans les éléments `<rule>`. Remplace l&#39;attribut::ClientAddressFilter lorsque la règle est appliquée.

## Attributs {#section-e7a0960f7f0045da91de37824aa4aeaa}

Aucune

## Données {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Liste d’adresses IP séparées par des virgules. Chaque adresse individuelle peut inclure un suffixe de masque de réseau facultatif pour permettre la spécification des plages d&#39;adresses IP. Voir ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` pour plus de détails.

## Description {#section-099b7839c4be40c68cbff29dad14e7d5}

L&#39;accès à ce catalogue d&#39;images peut être limité à une ou plusieurs adresses IP spécifiques en les spécifiant dans un élément `<addressfilter>`. Une erreur &quot;demande refusée&quot; est renvoyée au client si l’adresse IP du client n’est pas correspondante.

L&#39;accès n&#39;est pas restreint si `<addressfilter>` est vide ou non spécifié.

Si l&#39;élément `<expression>` de l&#39;élément `<rule>` est absent ou vide, l&#39;élément `<addressfilter>` est appliqué à toutes les requêtes.

`localhost` fait toujours implicitement partie de la  `ClientAddressFilter` définition, même si elle n’est pas explicitement spécifiée. Les demandes provenant de `localhost` ne sont jamais rejetées, quelle que soit la spécification `ClientAddressFilter`.

## SeeaAussi {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribut::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
