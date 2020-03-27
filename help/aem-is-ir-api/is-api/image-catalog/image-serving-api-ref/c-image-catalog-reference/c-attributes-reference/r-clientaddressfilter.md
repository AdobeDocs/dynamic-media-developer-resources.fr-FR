---
description: Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.
seo-description: Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.

Lorsqu’elles sont spécifiées, les demandes envoyées à ce catalogue d’images provenant d’un client à une adresse IP non répertoriée sont rejetées.

## Propriétés {#section-d785265988324af68835410c9ba54147}

d’adresses IP séparées par des virgules avec masques réseau facultatifs (la notation CIDR est utilisée) :

`*`ipAddress`*``[`/ *`netmask`*`]`*`[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>Adresse IP au format <span class="varname"> dd.ddd.ddd.ddd</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>Masque net (0...32). </p></td> 
 </tr> 
</table>

Cet attribut est ignoré lorsqu’une règle de prétraitement avec un `<addressfilter>` élément est appliquée.

## Par défaut {#section-de26e8c9225745e985e4beac1f03f4f6}

Héritée de `default::AddressFilter` si non définie ou si vide.

## Exemples {#section-a955314d2b6a4213a16c12a8b18d8627}

Aucune restriction d’accès : `0.0.0.0/0`

Accorder l&#39;accès à toutes les adresses à partir de 1992 : `192.0.0.0/8`

Octroyez l’accès aux 512 hôtes avec des adresses comprises entre 192.168.12.0 et 192.168.13.255 : `192.168.12.0/23`

Accorder l’accès à une adresse IP unique : `192.168.2.117` ou `192.168.2.117/32`

## Voir aussi {#section-4ea89a7d82e14a4a800487d2d8801465}

[adressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
