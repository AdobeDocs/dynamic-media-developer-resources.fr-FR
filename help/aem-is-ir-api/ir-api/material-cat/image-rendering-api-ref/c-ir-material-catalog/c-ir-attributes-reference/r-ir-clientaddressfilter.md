---
description: Filtre d’adresse IP du client. Permet la spécification d’une ou de plusieurs adresses IP ou plages d’adresses.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# ClientAddressFilter{#clientaddressfilter}

Filtre d’adresse IP du client. Permet la spécification d’une ou de plusieurs adresses IP ou plages d’adresses.

Lorsqu’elle est spécifiée, les requêtes envoyées à ce catalogue d’images provenant d’un client à une adresse IP non répertoriée sont rejetées. `localhost` fait toujours implicitement partie de la  `ClientAddressFilter` définition, même si elle n’est pas explicitement spécifiée. Les demandes provenant de `localhost` ne sont jamais rejetées, quelle que soit la spécification `ClientAddressFilter`.

## Propriétés {#section-21a2992f108d42fb8660c0d65aa61e13}

Liste d’adresses IP séparées par des virgules avec des masques réseau facultatifs ([la notation CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) est utilisée) :

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Adresse IP au  *[!DNL ddd.ddd.ddd.ddd]* format

* *[!DNL netmask]* masque de réseau (0...32)

Cet attribut est ignoré lorsqu’une règle de prétraitement avec un élément `<addressfilter>` est appliquée.

## Par défaut {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Hérité de `default::AddressFilter` si elle n&#39;est pas définie ou si elle est vide.

## Exemples {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Aucune restriction d&#39;accès : `0.0.0.0/0`
* Accorder l&#39;accès à toutes les adresses en commençant par `192: 192.0.0.0/8`
* Accorder l’accès aux 512 hôtes avec des adresses comprises entre `192.168.12.0` et `192.168.13.255: 192.168.12.0/23`

* Accorder l’accès à une seule adresse IP : `192.168.2.117` ou `192.168.2.117/32`

## Voir aussi {#section-6198780c7b3045aabd211eefb38bc565}

[adressfiltre](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
