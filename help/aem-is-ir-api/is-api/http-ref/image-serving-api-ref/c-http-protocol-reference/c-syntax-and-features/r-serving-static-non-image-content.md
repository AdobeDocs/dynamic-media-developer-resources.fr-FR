---
description: Diffusion de contenu statique (hors image)
solution: Experience Manager
title: Diffusion de contenu statique (hors image)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e2c79bdc-5d70-46d9-85f4-ffebd7621944
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# Diffusion de contenu statique (hors image){#serving-static-non-image-content}

La diffusion d’images fournit un mécanisme pour gérer les contenus autres que les images dans les catalogues et les diffuser par le biais d’un `context /is/content` distinct. Le mécanisme permet de configurer le délai d’activation séparément pour chaque élément.

## Syntaxe de base {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> requête </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http:// <span class="varname"> serveur </span>/is/content[/ <span class="varname"> catalogue </span>/ <span class="varname"> élément </span>][? <span class="varname"> modificateurs </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> serveur </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogue </span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant du catalogue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> élément </span> </span> </p> </td> 
  <td class="stentry"> <p>ID d’élément de contenu statique. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificateurs </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span>*[&amp; <span class="varname"> command </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> value </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span> </span> </p> </td> 
  <td class="stentry"> <p>Un des noms de commande pris en charge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de commande. </p> </td> 
 </tr> 
</table>

## Présentation des commandes {#section-61657a0141914053ab12038ad7e91500}

La diffusion d’images prend en charge les commandes suivantes à l’adresse /is/content :

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>Filtre de type de contenu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> et <span class="codeph"> req=exists </span> uniquement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache </a> </td> 
  <td class="stentry"> <p>Permet de désactiver la mise en cache côté client. </p> </td> 
 </tr> 
</table>

## Catalogues de contenu statique {#section-b2b8f4860fe84e528493ed704c7c5141}

Les catalogues de contenu statique sont similaires aux catalogues d’images, mais prennent en charge moins de champs de données :

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribute/Data</b> </th> 
   <th class="entry"> <b> Remarques</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> Catalogue <span class="codeph"> ::Id </span> </p> </td> 
   <td> <p> Identifiant d’enregistrement de catalogue pour cet élément de contenu statique </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td> <p> Chemin d’accès au fichier de cet élément de contenu </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> Catalogue <span class="codeph"> ::Expiration </span> </p> </td> 
   <td> <p> La durée de vie de cet élément de contenu ; attribute::Expiration est utilisée si non spécifié ou s’il est vide </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td> <p> Horodatage de modification du fichier ; requis lorsque la validation basée sur un catalogue est activée avec l’attribut ::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p> Métadonnées facultatives associées à cet élément de contenu statique ; disponibles pour le client avec req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td> <p> Type de données facultatif ; peut être utilisé pour filtrer les requêtes de contenu statique avec la commande type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrer le contenu statique {#section-896c37cf68bc446eb0766fb378898262}

Ce mécanisme peut permettre de s’assurer que les clients ne reçoivent que les contenus adaptés à leurs besoins. En supposant que le contenu statique soit balisé avec les valeurs `catalog::UserType` appropriées, le client peut ajouter la commande `type=` à la requête. La diffusion d’images compare la valeur fournie avec la commande `type=` à la valeur de `catalog::UserType` et, en cas de discordance, renvoie une erreur au lieu de contenus potentiellement inappropriés.

## Voir aussi {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Référence du catalogue d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
