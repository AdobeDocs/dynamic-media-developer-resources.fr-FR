---
description: Filtre d’adresses IP du client. Permet la spécification d’une ou de plusieurs adresses IP ou plages d’adresses.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

Filtre d’adresses IP du client. Permet la spécification d’une ou de plusieurs adresses IP ou plages d’adresses.

Lorsqu’elles sont spécifiées, les demandes adressées à ce catalogue d’images provenant d’un client à une adresse IP non répertoriée sont rejetées. `localhost` fait toujours implicitement partie de la variable `ClientAddressFilter` , même si elle n’est pas spécifiée explicitement. Demandes provenant de `localhost` ne sont jamais rejetés, quelle que soit la variable `ClientAddressFilter` spécification.

## Propriétés {#section-21a2992f108d42fb8660c0d65aa61e13}

Liste séparée par des virgules des adresses IP avec des netmasques facultatifs ([Notation CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) est utilisé) :

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Adresse IP dans *[!DNL ddd.ddd.ddd.ddd]* format

* *[!DNL netmask]* Masque net (0...32)

Cet attribut est ignoré lorsqu’une règle de prétraitement avec une `<addressfilter>` est appliqué.

## Par défaut {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Hérité de `default::AddressFilter` s’il n’est pas défini ou s’il est vide.

## Exemples {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Aucune restriction d’accès : `0.0.0.0/0`
* Accorder l’accès à toutes les adresses commençant par `192: 192.0.0.0/8`
* Accorder l’accès aux 512 hôtes avec des adresses entre `192.168.12.0` et `192.168.13.255: 192.168.12.0/23`

* Accorder l’accès à une seule adresse IP : `192.168.2.117` ou `192.168.2.117/32`

## Voir aussi {#section-6198780c7b3045aabd211eefb38bc565}

[address filter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
