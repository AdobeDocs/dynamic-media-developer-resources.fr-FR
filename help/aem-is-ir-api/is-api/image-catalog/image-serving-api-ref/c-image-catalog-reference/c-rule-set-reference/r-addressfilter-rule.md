---
description: Élément de filtre d’adresse. Facultatif dans les éléments <rule> et <pathrule>.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
TQID: 'https://experienceleague.adobe.com/NkzpvFZFbluayVtCa7qBVcSgY2aU5N7R2-rZkQCZHkw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 3%

---

# addressfilter{#addressfilter}

Élément de filtre d’adresse. Facultatif dans les éléments `<rule>` et `<pathrule>`.

Il remplace `attribute::ClientAddressFilter` lorsque la règle est appliquée.

## Attributs {#section-31e9ad29e9934933ac154bccbc729172}

Aucune

## Données {#section-c762bdfe425140d689ea5abf25e9a48a}

Liste d’adresses IP séparées par des virgules. Chaque adresse individuelle peut inclure un suffixe de masque de réseau facultatif pour permettre la spécification de plages d&#39;adresses IP. Voir `attribute::ClientAddressFilter` pour plus de détails.

## Description {#section-d561b2485e004ef8a2085997d0f4bca6}

L’accès à ce catalogue d’images peut être limité à une ou plusieurs adresses IP clientes spécifiques en les spécifiant dans un élément `<addressfilter>`. Une erreur de type « demande refusée » est renvoyée au client si l’adresse IP du client ne correspond pas.

L’accès n’est pas limité si `<addressfilter>` est vide ou non spécifié.

Si la `<expression>` dans l’élément `<rule>` est absente ou vide, la `<addressfilter>` est appliquée à toutes les requêtes.

## Voir aussi {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
