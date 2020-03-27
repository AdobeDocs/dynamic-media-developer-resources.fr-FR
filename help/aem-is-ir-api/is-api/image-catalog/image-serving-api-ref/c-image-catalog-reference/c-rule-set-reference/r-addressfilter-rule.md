---
description: Élément filtre d’adresse. Facultatif dans les éléments <rule> et <pathrule>.
seo-description: Élément filtre d’adresse. Facultatif dans les éléments <rule> et <pathrule>.
seo-title: adressfilter
solution: Experience Manager
title: adressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# adressfilter{#addressfilter}

Élément filtre d’adresse. Facultatif dans `<rule>` et `<pathrule>` les éléments.

Remplace `attribute::ClientAddressFilter` lorsque la règle est appliquée.

## Attributes {#section-31e9ad29e9934933ac154bccbc729172}

Aucune

## Données {#section-c762bdfe425140d689ea5abf25e9a48a}

d’adresses IP séparé par des virgules. Chaque adresse individuelle peut inclure un suffixe de masque de réseau facultatif afin de permettre la spécification des plages d&#39;adresses IP. See `attribute::ClientAddressFilter` for details.

## Description {#section-d561b2485e004ef8a2085997d0f4bca6}

L’accès à ce catalogue d’images peut être limité à une ou plusieurs adresses IP client spécifiques en les spécifiant dans un `<addressfilter>` élément. Une erreur &quot;demande refusée&quot; est renvoyée au client si l’adresse IP du client ne correspond pas.

L’accès n’est pas restreint si `<addressfilter>` il est vide ou non spécifié.

Si le `<expression>` contenu de l’ `<rule>` élément est absent ou vide, le `<addressfilter>` paramètre est appliqué à toutes les requêtes.

## Voir aussi {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribut::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
