---
description: Filtre d’adresse IP du client. Permet la spécification d’une ou de plusieurs adresses IP ou plages d’adresses.
solution: Experience Manager
title: ClientAddressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---


# ClientAddressFilter{#clientaddressfilter}

Filtre d’adresse IP du client. Permet la spécification d’une ou de plusieurs adresses IP ou plages d’adresses.

Lorsqu’elle est spécifiée, les requêtes envoyées à ce catalogue d’images provenant d’un client à une adresse IP non répertoriée sont rejetées.

## Propriétés {#section-d785265988324af68835410c9ba54147}

Liste d&#39;adresses IP séparées par des virgules avec des masques réseau facultatifs (la notation CIDR est utilisée) :

`*`ipAddress`*` `[`/  *`netmask`*`]`*  `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>Adresse IP au format <span class="varname"> ddd.ddd.ddd.ddd</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> masque réseau</span> </p></td> 
  <td class="stentry"> <p>Masque net (0...32). </p></td> 
 </tr> 
</table>

Cet attribut est ignoré lorsqu’une règle de prétraitement avec un élément `<addressfilter>` est appliquée.

## Par défaut {#section-de26e8c9225745e985e4beac1f03f4f6}

Hérité de `default::AddressFilter` si elle n&#39;est pas définie ou si elle est vide.

## Exemples {#section-a955314d2b6a4213a16c12a8b18d8627}

Aucune restriction d&#39;accès : `0.0.0.0/0`

Accorder l&#39;accès à toutes les adresses à partir de 192 : `192.0.0.0/8`

Accorder l&#39;accès aux 512 hôtes avec des adresses comprises entre 192.168.12.0 et 192.168.13.255 : `192.168.12.0/23`

Accorder l’accès à une seule adresse IP : `192.168.2.117` ou `192.168.2.117/32`

## Voir aussi {#section-4ea89a7d82e14a4a800487d2d8801465}

[adressfiltre](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
