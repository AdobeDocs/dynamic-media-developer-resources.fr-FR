---
title: id
description: Version de l’image/métadonnées. Lorsque vous travaillez avec du contenu qui change fréquemment, les serveurs des réseaux de mise en cache tels qu’Akamai, les caches de navigateur et les caches de serveurs proxy d’entreprise peuvent stocker des réponses Image Serving qui peuvent être obsolètes pendant un certain temps.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 3%

---

# id{#id}

Version de l’image/métadonnées. Lorsque vous travaillez avec du contenu qui change fréquemment, les serveurs des réseaux de mise en cache tels qu’Akamai, les caches de navigateur et les caches de serveurs proxy d’entreprise peuvent stocker des réponses Image Serving qui peuvent être obsolètes pendant un certain temps.

` id= *`Val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Val </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne de version. </p> </td> 
 </tr> 
</table>

Image Serving inclut un mécanisme de contrôle de version qui peut aider à réduire le risque qu’une entrée de cache obsolète soit utilisée par une application. Ce mécanisme consiste à utiliser `req=props` pour obtenir des chaînes d’identification de version pour les données d’image et les métadonnées (telles que les données de zone cliquable ou de cible de zoom). La chaîne d’identifiant de version est ensuite ajoutée aux demandes de diffusion d’images pouvant être mises en cache avec la `id=` commande.

Lorsqu’une image source ou des métadonnées changent, la valeur d’ID de version correspondante change également. L’inclusion d’une valeur d’ID de version à jour avec la commande garantit que les `id=` anciennes entrées de cache ne sont plus accessibles.

Le tableau suivant répertorie les chaînes d’identifiant de version à utiliser pour chaque `req=` type :

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> Identifiant de version : req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> carte </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> masque </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> cibles </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Données utilisateur </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> d’écriture différée xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` Les types non répertoriés ci-dessus ont une durée de vie courte ( `attribute::NonImgExpiration`) ou leurs réponses ne peuvent pas du tout être mises en cache ; il n’y a aucun avantage à inclure `id=` avec de telles requêtes.

## Propriétés {#section-62e973d0d5884abebbb0679f9278ae2c}

Attribut de requête. Optionnel. Toujours ignoré par le serveur.

## Par défaut {#section-96136720c82842c89505347ec39e6024}

Aucune

## Exemple {#section-a5fb871e0ec8485c91c4fca78895d17f}

Voir la description de rect=[ pour un exemple d’utilisation](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3).

## Voir également {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalogue ::Expiration, ](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)attribut[ ::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
