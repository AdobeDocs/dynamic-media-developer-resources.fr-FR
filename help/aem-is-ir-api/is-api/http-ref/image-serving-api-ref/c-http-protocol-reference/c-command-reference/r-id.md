---
title: id
description: Version de l’image/des métadonnées. Lorsque vous travaillez avec du contenu qui change fréquemment, les serveurs des réseaux de mise en cache tels qu’Akamai, les caches de navigateur et les caches de serveur proxy d’entreprise peuvent stocker des réponses de diffusion d’images qui peuvent être obsolètes pendant certaines périodes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
TQID: 'https://experienceleague.adobe.com/TPRGzHQ-TxTusgeqo2eLlCG0fNOtmJ1IHIxuUy8bh2I'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 3%

---

# id{#id}

Version de l’image/des métadonnées. Lorsque vous travaillez avec du contenu qui change fréquemment, les serveurs des réseaux de mise en cache tels qu’Akamai, les caches de navigateur et les caches de serveur proxy d’entreprise peuvent stocker des réponses de diffusion d’images qui peuvent être obsolètes pendant certaines périodes.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Chaîne de version. </p> </td> 
 </tr> 
</table>

La diffusion d’images comprend un mécanisme de contrôle de version qui peut contribuer à réduire les risques qu’une entrée de cache obsolète soit utilisée par une application. Ce mécanisme implique l’utilisation de `req=props` pour obtenir des chaînes d’identifiant de version pour les données d’image et les métadonnées (telles que les données de la zone cliquable ou les données de la cible de zoom). La chaîne d’identifiant de version est ensuite ajoutée aux requêtes de diffusion d’images pouvant être mises en cache avec la commande `id=`.

Lorsqu’une image ou des métadonnées source sont modifiées, la valeur d’identifiant de version correspondante change également. L’inclusion d’une valeur d’identifiant de version à jour avec la commande `id=` garantit que les anciennes entrées de cache ne sont plus accessibles.

Le tableau suivant répertorie les chaînes d’identifiant de version à utiliser pour chaque type de `req=` :

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type </b> </th> 
   <th class="entry"> <b> de version de req=props</b> </th> 
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
   <td> <p> œillet </p> </td> 
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

Les types de `req=` non répertoriés ci-dessus ont une durée de vie courte ( `attribute::NonImgExpiration`) ou leurs réponses ne peuvent pas du tout être mises en cache. Il n’y a aucun avantage à inclure des `id=` avec de telles requêtes.

## Propriétés {#section-62e973d0d5884abebbb0679f9278ae2c}

Attribut de requête. Facultatif. Toujours ignoré par le serveur.

## Par défaut {#section-96136720c82842c89505347ec39e6024}

Aucune

## Exemple {#section-a5fb871e0ec8485c91c4fca78895d17f}

Voir la description de [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) pour obtenir un exemple d’utilisation.

## Voir également {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
