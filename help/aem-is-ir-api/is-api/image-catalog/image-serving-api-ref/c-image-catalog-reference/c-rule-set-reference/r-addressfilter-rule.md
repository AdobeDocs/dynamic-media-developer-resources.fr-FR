---
description: Élément de filtre d’adresse. Facultatif dans les éléments <rule> et <pathrule>.
solution: Experience Manager
title: address filter
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# address filter{#addressfilter}

Élément de filtre d’adresse. Facultatif dans les éléments `<rule>` et `<pathrule>` .

Remplace `attribute::ClientAddressFilter` lorsque la règle est appliquée.

## Attributs {#section-31e9ad29e9934933ac154bccbc729172}

Aucune

## Données {#section-c762bdfe425140d689ea5abf25e9a48a}

Liste d’adresses IP séparées par des virgules. Chaque adresse individuelle peut inclure un suffixe de masque de réseau facultatif afin de permettre la spécification des plages d’adresses IP. Voir `attribute::ClientAddressFilter` pour plus de détails.

## Description {#section-d561b2485e004ef8a2085997d0f4bca6}

L&#39;accès à ce catalogue d&#39;images peut être limité à une ou plusieurs adresses IP client spécifiques en les spécifiant dans un élément `<addressfilter>` . Une erreur &quot;demande refusée&quot; est renvoyée au client si l’adresse IP du client n’est pas correspondante.

L’accès n’est pas restreint si `<addressfilter>` est vide ou non spécifié.

Si la valeur `<expression>` de l’élément `<rule>` est absente ou vide, la valeur `<addressfilter>` est appliquée à toutes les requêtes.

## Voir aussi {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
