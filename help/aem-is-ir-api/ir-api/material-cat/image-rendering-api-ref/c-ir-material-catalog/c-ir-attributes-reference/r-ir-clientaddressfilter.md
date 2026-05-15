---
title: ClientAddressFilter
description: Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
TQID: 'https://experienceleague.adobe.com/azMITpRcITTOEB0FCev6vWiTmocumP-0HTQD3rIV-fA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 2%

---

# ClientAddressFilter{#clientaddressfilter}

Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.

Lorsqu’elles sont spécifiées, les requêtes adressées à ce catalogue d’images provenant d’un client à une adresse IP non répertoriée sont rejetées. `localhost` fait toujours implicitement partie de la définition du `ClientAddressFilter`, même si elle n’est pas explicitement spécifiée. Les requêtes provenant de `localhost` ne sont jamais rejetées, quelle que soit la spécification `ClientAddressFilter`.

## Propriétés {#section-21a2992f108d42fb8660c0d65aa61e13}

Liste d’adresses IP séparées par des virgules avec des masques de réseau facultatifs (la notation [CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) est utilisée) :

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* IP au format *[!DNL ddd.ddd.ddd.ddd]*

* *[!DNL netmask]* masque de réseau (0...32)

Cet attribut est ignoré lorsqu’une règle de pré-traitement avec un élément `<addressfilter>` est appliquée.

## Par défaut {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Hérité de `default::AddressFilter` si non défini ou si vide.

## Exemples {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Aucune restriction d’accès : `0.0.0.0/0`
* Accorder l&#39;accès à toutes les adresses commençant par `192: 192.0.0.0/8`
* Octroi de l’accès aux 512 hôtes avec des adresses comprises entre `192.168.12.0` et `192.168.13.255: 192.168.12.0/23`

* Accorder l&#39;accès à une seule adresse IP : `192.168.2.117` ou `192.168.2.117/32`

## Voir aussi {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
