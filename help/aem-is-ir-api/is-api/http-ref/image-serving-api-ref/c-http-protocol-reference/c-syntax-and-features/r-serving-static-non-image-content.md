---
description: Diffusion de contenu statique (hors images)
solution: Experience Manager
title: Diffusion de contenu statique (hors images)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
TQID: 'https://experienceleague.adobe.com/fWwGD0B2IS6rd7Ls6rEb2RzH82e-lFHS2WUBrNGe7QY'
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
source-wordcount: 291
ht-degree: 0%

---

# Diffusion de contenu statique (hors images){#serving-static-non-image-content}

La diffusion d’images fournit un mécanisme de gestion des contenus non-images dans les catalogues et les diffuse au moyen d’un `context /is/content` distinct. Le mécanisme permet de configurer la TTL pour chaque élément séparément.

## Syntaxe de base {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> requête </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> serveur </span>/is/content[/ <span class="varname"> catalogue </span>/ <span class="varname"> élément </span>][ ? <span class="varname"> modificateurs </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> serveur <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[: <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogue </span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant du catalogue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> élément </span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant d’élément de contenu statique. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificateurs </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> commande </span>*[&amp; <span class="varname"> commande </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> commande </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> valeur </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Un des noms de commande pris en charge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> valeur <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de la commande. </p> </td> 
 </tr> 
</table>

## Présentation des commandes {#section-61657a0141914053ab12038ad7e91500}

Le service d’images prend en charge les commandes suivantes sous /is/content :

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>Filtre du type de contenu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> et <span class="codeph"> req=exists </span> uniquement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> </a> du cache <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> </td> 
  <td class="stentry"> <p>Permet de désactiver le cache côté client. </p> </td> 
 </tr> 
</table>

## Catalogues de contenu statiques {#section-b2b8f4860fe84e528493ed704c7c5141}

Les catalogues de contenu statique sont similaires aux catalogues d’images, mais prennent en charge moins de champs de données :

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Données</b> </th> 
   <th class="entry"> <b> notes</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td> <p> Identifiant d’enregistrement de catalogue pour cet élément de contenu statique </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td> <p> Chemin d’accès au fichier pour cet élément de contenu </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td> <p> Durée de vie de cet élément de contenu ; attribute::Expiration est utilisé si non spécifié ou si vide </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td> <p> Horodatage de modification du fichier ; obligatoire lorsque la validation basée sur le catalogue est activée avec l’attribut attribute::CacheValidationPolicy. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p> Métadonnées facultatives associées à cet élément de contenu statique ; disponibles pour le client avec req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> Type de données facultatif. Peut être utilisé pour filtrer les requêtes de contenu statique avec la commande type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrer du contenu statique {#section-896c37cf68bc446eb0766fb378898262}

Ce mécanisme permet de s’assurer que les clients ne reçoivent que le contenu adapté à leurs besoins. En supposant que le contenu statique soit balisé avec les valeurs `catalog::UserType` appropriées, le client peut ajouter la commande `type=` à la requête. La diffusion d’images compare la valeur fournie avec la commande `type=` à la valeur de `catalog::UserType` et, en cas de non-correspondance, renvoie une erreur au lieu de contenus potentiellement inappropriés.

## Voir aussi {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Référence du catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
