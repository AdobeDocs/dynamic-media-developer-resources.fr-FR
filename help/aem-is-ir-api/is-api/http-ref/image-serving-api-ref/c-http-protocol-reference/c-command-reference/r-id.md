---
description: Version de l’image/des métadonnées. Lorsque vous travaillez avec du contenu qui change fréquemment, les serveurs des réseaux de mise en cache tels qu’Akamai, les caches de navigateur et les caches de serveur proxy d’entreprise peuvent stocker des réponses Image Serving qui peuvent être obsolètes pendant des périodes.
solution: Experience Manager
title: id
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 4%

---


# id{#id}

Version de l’image/des métadonnées. Lorsque vous travaillez avec du contenu qui change fréquemment, les serveurs des réseaux de mise en cache tels qu’Akamai, les caches de navigateur et les caches de serveur proxy d’entreprise peuvent stocker des réponses Image Serving qui peuvent être obsolètes pendant des périodes.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne de version. </p> </td> 
 </tr> 
</table>

La diffusion d’images comprend un mécanisme de gestion des versions qui peut aider à réduire le risque d’utilisation d’une entrée de cache obsolète par une application. Ce mécanisme implique l’utilisation de `req=props` pour obtenir des chaînes d’identifiant de version pour les données d’image et les métadonnées (telles que les données de zone cliquable ou de cible de zoom). La chaîne d’identifiant de version est ensuite ajoutée aux demandes Image Serving pouvant être mises en cache avec la commande `id=`.

Lorsqu’une image source ou des métadonnées changent, la valeur d’ID de version correspondante change également. L’inclusion d’une valeur d’ID de version à jour avec la commande `id=` garantit que les anciennes entrées de cache ne seront plus accessibles.

Le tableau suivant liste les chaînes d&#39;identifiant de version à utiliser pour chaque type `req=` :

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> identificateur de version de req=props</b> </th> 
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
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` les types non énumérés ci-dessus ont un TTL court (  `attribute::NonImgExpiration`) ou leurs réponses ne peuvent pas être mises en cache ; il n&#39;y a aucun avantage à inclure  `id=` de telles demandes.

## Propriétés {#section-62e973d0d5884abebbb0679f9278ae2c}

Attribut de requête. Facultatif. Toujours ignorée par le serveur.

## Par défaut {#section-96136720c82842c89505347ec39e6024}

Aucune

## Exemple {#section-a5fb871e0ec8485c91c4fca78895d17f}

Voir la description de [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), par exemple l’utilisation.

## Voir également {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [attribut::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
