---
description: Vous pouvez utiliser Image Serving pour gérer le contenu sans image dans les catalogues et l’utiliser dans un contexte /is/content distinct.
seo-description: Vous pouvez utiliser Image Serving pour gérer le contenu sans image dans les catalogues et l’utiliser dans un contexte /is/content distinct.
seo-title: Diffusion de contenu statique (sans image)
solution: Experience Manager
title: Diffusion de contenu statique (sans image)
topic: Scene7 Image Serving - Image Rendering API
uuid: bdb1383a-e02d-499f-be79-4a6dc501705c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Diffusion de contenu statique (sans image){#serving-static-non-image-contents}

Vous pouvez utiliser Image Serving pour gérer le contenu sans image dans les catalogues et l’utiliser dans un contexte /is/content distinct.

Cette fonctionnalité permet de configurer le TTL pour chaque élément séparément.

Image Serving prend en charge les commandes suivantes dans [!DNL /is/content]:

<table id="simpletable_8A3AB1D1D20F4B6CBE86767E94735980"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" format="dita" scope="local"> type </a> </p> </td> 
  <td class="stentry"> <p>Filtre de type de contenu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" format="dita" scope="local"> req </a> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata </span>, <span class="codeph"> req=props </span>et <span class="codeph"> req=exists </span> uniquement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" format="dita" scope="local"> cache </a> </p> </td> 
  <td class="stentry"> <p>Permet de désactiver la mise en cache côté client. </p> </td> 
 </tr> 
</table>

## Syntaxe de base {#section-42103439011540b2b9da3b5eebb442cd}

<table id="simpletable_2F039A5BFA2C4E22B014F42ECBCDA0A2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> demande </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="filepath"> http:// <span class="varname"> serveur </span>/is/content[/catalog/ <span class="varname"> élément </span>][? <span class="varname"> modificateurs </span>] </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address </span>[ : <span class="varname"> port </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogue </span></span> </p> </td> 
  <td class="stentry"> <p>Identifiant du catalogue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> élément </span></span> </p> </td> 
  <td class="stentry"> <p>ID d’élément de contenu statique. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificateurs </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> , commande </span>*[&amp; <span class="varname"> commande </span>] </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> , commande </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span>= <span class="varname"> valeur </span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName </span></span> </p> </td> 
  <td class="stentry"> <p>Un des noms de commande pris en charge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valeur </span></span> </p> </td> 
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
   <td colname="col2"> <p>Identificateur d’enregistrement du catalogue pour cet élément de contenu statique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogue ::Chemin </span> </p> </td> 
   <td colname="col2"> <p>Chemin du fichier pour cet élément de contenu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogue ::Expiration </span> </p> </td> 
   <td colname="col2"> <p>TTL pour cet élément de contenu ; <span class="codeph"> attribute::Expiration </span> est utilisée si elle n’est pas spécifiée ou si elle est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogue::TimeStamp </span> </p> </td> 
   <td colname="col2"> <p>Horodatage de modification de fichier; requise lorsque la validation basée sur un catalogue est activée avec <span class="codeph"> attribut::CacheValidationPolicy </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalogue::UserData </span> </p> </td> 
   <td colname="col2"> <p>Métadonnées facultatives associées à cet élément de contenu statique ; disponible pour le client avec <span class="codeph"> req=userdata </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> catalog::UserType </span> </p> </td> 
   <td colname="col2"> <p>Type de données facultatif ; peut être utilisée pour filtrer les requêtes de contenu statique avec la commande <span class="codeph"> type= </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrage du contenu statique {#section-4c41bf41ff994910840c1352683d1f37}

Ce mécanisme permet de s&#39;assurer que les clients reçoivent uniquement le contenu adapté à leurs besoins. En supposant que le contenu statique soit balisé avec les `catalog::UserType` valeurs appropriées, le client peut ajouter la `type=` commande à la requête. Image Serving compare la valeur fournie avec la `type=` commande à la valeur de `catalog::UserType` et, en cas de discordance, renvoie une erreur au lieu d’un contenu potentiellement inapproprié.

## Fichiers de sous-titrage vidéo {#section-1ad25e10399e43eaa8ecb09b531dbf1a}

Vous pouvez encapsuler des fichiers de sous-titrage vidéo (WebVTT), CSS ou tout autre fichier texte au format JSONP. La réponse JSON est décrite ci-dessous.

* Pour les fichiers WebVTT, le type mime de la réponse est text/javascript. JSON n’est pas renvoyé ; au lieu de cela, Javascript est renvoyé et appelle une méthode avec JSON. L’ID et le gestionnaire sont facultatifs.
* Pour les fichiers CSS, le type mime de la réponse est text/javascript. L’ID et le gestionnaire sont facultatifs.
* Par défaut, le codage UTF-8 est appliqué pour s’assurer qu’il est correctement décodé. La taille maximale par défaut est de 2 Mo.

Vous pouvez également utiliser des pistes pour d’autres types de métadonnées temporisées. Les données source de chaque élément de suivi sont un fichier texte constitué d’un de signaux temporels. Les repères peuvent inclure des données dans des formats tels que JSON ou CSV.

Voir [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) pour plus d’informations sur le format JSONP.

Voir [www.json.org](http://www.json.org) pour plus d’informations sur le format JSON.

## Voir aussi {#section-7b28631016044a22a3a6762fd64771e9}

[type=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) , [req=](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), référence du catalogue [d’images](../../is-api/image-serving-api-ref/c-image-catalog-reference/c-image-catalog-reference.md#concept-e23d45ea3abe43119d5144e01c14b0b5)
