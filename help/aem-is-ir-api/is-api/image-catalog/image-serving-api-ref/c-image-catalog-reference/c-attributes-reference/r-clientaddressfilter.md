---
description: Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
TQID: 'https://experienceleague.adobe.com/cQT0eRo0amqhX76H3dNZakwlGsKt3-MAkIsRZytyREI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.

Lorsqu’elles sont spécifiées, les requêtes adressées à ce catalogue d’images provenant d’un client à une adresse IP non répertoriée sont rejetées.

## Propriétés {#section-d785265988324af68835410c9ba54147}

Liste d’adresses IP séparées par des virgules avec des masques réseau facultatifs (la notation CIDR est utilisée) :

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>Adresse IP au format <span class="varname"> ddd.ddd.ddd.ddd</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> un masque de réseau</span> </p></td> 
  <td class="stentry"> <p>Masque de réseau (0...32). </p></td> 
 </tr> 
</table>

Cet attribut est ignoré lorsqu’une règle de prétraitement avec un élément `<addressfilter>` est appliquée.

## Par défaut {#section-de26e8c9225745e985e4beac1f03f4f6}

Hérité de `default::AddressFilter` si non défini ou si vide.

## Exemples {#section-a955314d2b6a4213a16c12a8b18d8627}

Aucune restriction d’accès : `0.0.0.0/0`

Accorder l&#39;accès à toutes les adresses commençant par 192 : `192.0.0.0/8`

Accordez l’accès aux 512 hôtes dont les adresses sont comprises entre 192.168.12.0 et 192.168.13.255 : `192.168.12.0/23`

Accorder l&#39;accès à une seule adresse IP : `192.168.2.117` ou `192.168.2.117/32`

## Voir aussi {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
