---
description: Élément de filtre d’adresses. Facultatif dans les éléments <rule> et <pathrule>.
solution: Experience Manager
title: adressfiltre
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# address filter{#addressfilter}

Élément de filtre d’adresses. Facultatif dans les éléments `<rule>` et `<pathrule>`.

Remplace `attribute::ClientAddressFilter` lorsque la règle est appliquée.

## Attributs {#section-31e9ad29e9934933ac154bccbc729172}

Aucune

## Données {#section-c762bdfe425140d689ea5abf25e9a48a}

Liste d’adresses IP séparées par des virgules. Chaque adresse individuelle peut inclure un suffixe de masque de réseau facultatif pour permettre la spécification des plages d&#39;adresses IP. Voir `attribute::ClientAddressFilter` pour plus de détails.

## Description {#section-d561b2485e004ef8a2085997d0f4bca6}

L&#39;accès à ce catalogue d&#39;images peut être limité à une ou plusieurs adresses IP client spécifiques en les spécifiant dans un élément `<addressfilter>`. Une erreur &quot;demande refusée&quot; est renvoyée au client si l’adresse IP du client n’est pas correspondante.

L&#39;accès n&#39;est pas restreint si `<addressfilter>` est vide ou non spécifié.

Si l&#39;élément `<expression>` de l&#39;élément `<rule>` est absent ou vide, l&#39;élément `<addressfilter>` est appliqué à toutes les requêtes.

## Voir aussi {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribut::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
