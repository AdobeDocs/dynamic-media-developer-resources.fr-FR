---
title: Diffusion de contenu statique (hors images)
description: Vous pouvez utiliser la Diffusion d’images pour gérer le contenu non-image dans les catalogues et le diffuser au moyen d’un contexte /is/content distinct.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Diffusion de contenu statique (hors images){#serving-static-non-image-contents}

Vous pouvez utiliser la Diffusion d’images pour gérer le contenu non-image dans les catalogues et le diffuser au moyen d’un contexte /is/content distinct.

Cette fonctionnalité permet de configurer la TTL pour chaque élément séparément.

La diffusion d’images prend en charge les commandes suivantes à l’[!DNL /is/content] :

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Filtre du type de contenu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span> et <span class="codeph"> req=exists </span> uniquement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> du cache </a> </p> </td> 
  <td class="stentry"> <p>Permet de désactiver le cache côté client. </p> </td> 
 </tr> 
</table>

## Syntaxe de base {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> requête </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> serveur </span>/is/content[/catalog/ <span class="varname"> item </span>][ ? <span class="varname"> modificateurs </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> serveur <span class="varname"> </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
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

## Catalogues de contenu statiques {#section-91014f17f0d543d7aaf24539b2d7d4b9}

Les catalogues de contenu statique sont similaires aux catalogues d’images, mais prennent en charge moins de champs de données :

<table id="table_71A565DF5EC94913AD35CB13B0C7A27D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attribut/Données </p> </th> 
   <th colname="col2" class="entry"> <p>Remarques </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Id </span> </p> </td> 
   <td colname="col2"> <p>Identifiant d’enregistrement de catalogue pour cet élément de contenu statique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Path </span> </p> </td> 
   <td colname="col2"> <p>Chemin d’accès au fichier pour cet élément de contenu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::Expiration </span> </p> </td> 
   <td colname="col2"> <p>Durée de vie de cet élément de contenu ; <span class="codeph"> attribut::Expiration </span> est utilisé s’il n’est pas spécifié ou s’il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Horodatage de modification du fichier. Obligatoire lorsque la validation basée sur le catalogue est activée avec <span class="codeph"> attribut::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td colname="col2"> <p>Métadonnées facultatives associées à cet élément de contenu statique ; disponibles pour le client avec <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Type de données facultatif. Peut être utilisé pour filtrer les requêtes de contenu statique avec la <span class="codeph"> de commande </span> type= . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrer du contenu statique {#section-4c41bf41ff994910840c1352683d1f37}

Ce mécanisme permet de s’assurer que les clients ne reçoivent que le contenu adapté à leurs besoins. En supposant que le contenu statique soit balisé avec les valeurs de `catalog::UserType` appropriées, le client peut ajouter la commande `type=` à la requête. La diffusion d’images compare la valeur fournie avec la commande `type=` à la valeur de `catalog::UserType` et, en cas de non-correspondance, renvoie une erreur au lieu de contenus potentiellement inappropriés.

## Fichiers de légendes vidéo {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Vous pouvez encapsuler des fichiers de sous-titres vidéo (WebVTT), CSS ou tout autre fichier texte au format JSONP. La réponse JSON est décrite ci-dessous.

* Pour les fichiers WebVTT, le type MIME de la réponse est text/javascript. JSON n’est pas renvoyé ; à la place, JavaScript est renvoyé, qui appelle une méthode avec JSON. L’ID et le gestionnaire sont facultatifs.
* Pour les fichiers CSS, le type MIME de la réponse est text/javascript. L’ID et le gestionnaire sont facultatifs.
* Par défaut, le codage UTF-8 est appliqué pour s’assurer qu’il est correctement décodé. La limite de taille par défaut est de 2 Mo.

Vous pouvez également utiliser des pistes pour d’autres types de métadonnées horodatées. Les données sources de chaque élément de suivi sont un fichier texte composé d’une liste de repères horodatés. Les indices peuvent inclure des données dans des formats tels que JSON ou CSV.

Voir [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) pour plus d’informations sur le format JSONP.

Voir [www.json.org](https://www.json.org/json-en.html) pour plus d’informations sur le format JSON.

## Voir aussi {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Référence du catalogue d’images](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
