---
description: Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

Filtre d’adresse IP du client. Permet de spécifier une ou plusieurs adresses IP ou plages d’adresses.

Lorsque spécifié, les demandes adressées à ce catalogue d’images qui proviennent d’un client à une adresse IP non répertoriée sont rejetées.

## Propriétés {#section-d785265988324af68835410c9ba54147}

Liste d’adresses IP séparées par des virgules avec masques de réseau facultatifs (la notation CIDR est utilisée) :

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> Adresse IP</span> </p> </td> 
  <td class="stentry"> <p>Adresse IP au <span class="varname"> format ddd.ddd.ddd.ddd.</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> masque de réseau</span> </p></td> 
  <td class="stentry"> <p>Masque de réseau (0... 32). </p></td> 
 </tr> 
</table>

Cet attribut est ignoré lorsqu’une règle de prétraitement avec un `<addressfilter>` élément est appliquée.

## Par défaut {#section-de26e8c9225745e985e4beac1f03f4f6}

Hérité de `default::AddressFilter` si non défini ou si vide.

## Exemples {#section-a955314d2b6a4213a16c12a8b18d8627}

Aucune restriction d’accès : `0.0.0.0/0`

Accorder l’accès à toutes les adresses commençant par 192 : `192.0.0.0/8`

Accordez l’accès aux hôtes 512 dont les adresses sont comprises entre 192.168.12.0 et 192.168.13.255: `192.168.12.0/23`

Accorder l’accès à une seule adresse IP : `192.168.2.117` ou `192.168.2.117/32`

## Voir aussi {#section-4ea89a7d82e14a4a800487d2d8801465}

[Filtre d’adresse](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
