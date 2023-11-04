---
title: Diffusion de contenu statique (hors image)
description: Vous pouvez utiliser le service d’images pour gérer le contenu non-image dans les catalogues et l’afficher par le biais d’un contexte /is/content distinct.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: adc3d972-b02d-40db-992e-acaa06b848ff
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 1%

---

# Diffusion de contenu statique (hors image){#serving-static-non-image-contents}

Vous pouvez utiliser le service d’images pour gérer le contenu non-image dans les catalogues et l’afficher par le biais d’un contexte /is/content distinct.

Cette fonctionnalité permet de configurer le délai d’activation séparément pour chaque élément.

La diffusion d’images prend en charge les commandes suivantes à l’adresse [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Filtre de type de contenu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>, et <span class="codeph"> req=exists </span> uniquement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>Permet de désactiver la mise en cache côté client. </p> </td> 
 </tr> 
</table>

## Syntaxe de base {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> requête </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> server </span>/is/content[/catalog/ <span class="varname"> item </span>][? <span class="varname"> modificateurs </span>] </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogue </span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant du catalogue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item </span> </span> </p> </td> 
  <td class="stentry"> <p>ID d’élément de contenu statique. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificateurs </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command </span>*&amp; <span class="varname"> command </span>] </span> </p> </td> 
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

## Catalogues de contenu statique {#section-91014f17f0d543d7aaf24539b2d7d4b9}

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
   <td colname="col1"> <p> <span class="codeph"> catalogue : Expiration </span> </p> </td> 
   <td colname="col2"> <p>TTL pour cet élément de contenu ; <span class="codeph"> attribute::Expiration </span> est utilisé s’il n’est pas spécifié ou s’il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogue ::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Horodatage de modification de fichier ; requis lorsque la validation basée sur un catalogue est activée avec <span class="codeph"> attribute::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogue ::UserData </span> </p> </td> 
   <td colname="col2"> <p>Métadonnées facultatives associées à cet élément de contenu statique ; disponibles pour le client avec <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Type de données facultatif ; peut être utilisé pour filtrer les requêtes de contenu statique avec le <span class="codeph"> type= commande </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrer le contenu statique {#section-4c41bf41ff994910840c1352683d1f37}

Ce mécanisme peut permettre de s’assurer que les clients ne reçoivent que les contenus adaptés à leurs besoins. En supposant que le contenu statique soit balisé avec les balises appropriées `catalog::UserType` , le client peut ajouter la variable `type=` à la requête. Le serveur d’images compare la valeur fournie avec la variable `type=` à la valeur de `catalog::UserType` et, en cas de discordance, renvoie une erreur au lieu de contenus potentiellement inappropriés.

## Fichiers de sous-titres vidéo {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Vous pouvez encapsuler des fichiers de sous-titres vidéo (WebVTT), CSS ou tout fichier texte au format JSONP. La réponse JSON est décrite ci-dessous.

* Pour les fichiers WebVTT, le type MIME de la réponse est text/javascript. JSON n’est pas renvoyé. Au lieu de cela, JavaScript est renvoyé qui appelle une méthode avec JSON. L’identifiant et le gestionnaire sont facultatifs.
* Pour les fichiers CSS, le type MIME de la réponse est text/javascript. L’identifiant et le gestionnaire sont facultatifs.
* Par défaut, le codage UTF-8 est appliqué pour s’assurer qu’il est décodé correctement. La taille par défaut est limitée à 2 Mo.

Vous pouvez également utiliser des traces pour d’autres types de métadonnées minutées. Les données source de chaque élément de suivi sont un fichier texte constitué d’une liste de repères minutés. Les repères peuvent inclure des données dans des formats tels que JSON ou CSV.

Voir [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP) pour plus d’informations sur le format JSONP.

Voir [www.json.org](https://www.json.org/json-en.html) pour plus d’informations sur le format JSON.

## Voir aussi {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Référence du catalogue d’images](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
