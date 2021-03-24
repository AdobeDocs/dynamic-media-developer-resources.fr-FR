---
description: Diffusion de contenu statique (sans image)
solution: Experience Manager
title: Diffusion de contenu statique (sans image)
feature: Dynamic Media Classic, SDK/API
role: Développeur, Professionnel
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# Diffusion de contenu statique (sans image){#serving-static-non-image-content}

La diffusion d’images offre un mécanisme de gestion du contenu sans image dans les catalogues et de diffusion via un `context /is/content` distinct. Ce mécanisme permet de configurer le TTL pour chaque élément séparément.

## Syntaxe de base {#section-a986baaca8644d04bcd0ddf781ae916e}

<table id="simpletable_4A6249F0C40747339524323EB0831CE4"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> demander  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> http://  <span class="varname"> server  </span>/is/content[/  <span class="varname"> catalog  </span>/  <span class="varname"> item  </span>][ ? <span class="varname"> modificateurs  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address  </span>[ :  <span class="varname"> port  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> catalogue  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identifiant du catalogue. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> item  </span> </span> </p> </td> 
  <td class="stentry"> <p>ID de l’élément de contenu statique. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> modificateurs  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> commande  </span>*[&amp;  <span class="varname"> commande  </span>]  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> command  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span>=  <span class="varname"> valeur  </span> </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cmdName  </span> </span> </p> </td> 
  <td class="stentry"> <p>Un des noms de commande pris en charge. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valeur de commande. </p> </td> 
 </tr> 
</table>

## Présentation des commandes {#section-61657a0141914053ab12038ad7e91500}

Image Serving prend en charge les commandes suivantes dans /is/content :

<table id="simpletable_1D96BA1AB5394B3C9B91D46617AFC0FA"> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb" type="reference" format="dita" scope="local"> type </a> </td> 
  <td class="stentry"> <p>Filtre de type de contenu. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req  </a> </td> 
  <td class="stentry"> <p> <span class="codeph"> req=userdata  </span>,  <span class="codeph"> req=props  </span>et  <span class="codeph"> req=exists  </span> uniquement. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <a href="../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-cache.md#reference-168189bee4ce4d1189d427891f22be2e" type="reference" format="dita" scope="local"> cache  </a> </td> 
  <td class="stentry"> <p>Permet de désactiver la mise en cache côté client. </p> </td> 
 </tr> 
</table>

## Catalogues de contenu statique {#section-b2b8f4860fe84e528493ed704c7c5141}

Les catalogues de contenu statique sont similaires aux catalogues d’images, mais prennent en charge moins de champs de données :

<table id="table_3B111EC3AA1044FB9B659FD54BADDC39"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> Attribut/Données</b> </th> 
   <th class="entry"> <b> Remarques</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::Id  </span> </p> </td> 
   <td> <p> Identificateur d'enregistrement de catalogue pour cet élément de contenu statique </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue : chemin  </span> </p> </td> 
   <td> <p> Chemin d'accès au fichier pour cet élément de contenu </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::Expiration  </span> </p> </td> 
   <td> <p> TTL pour cet élément de contenu ; attribute::Expiration est utilisée si non spécifié ou si vide </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::TimeStamp  </span> </p> </td> 
   <td> <p> Horodatage de modification du fichier ; requis lorsque la validation basée sur un catalogue est activée avec attribut::CacheValidationPolicy </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::UserData  </span> </p> </td> 
   <td> <p> Métadonnées facultatives associées à cet élément de contenu statique ; disponible pour le client avec req=userdata </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogue ::UserType  </span> </p> </td> 
   <td> <p> Type de données facultatif ; peut être utilisé pour filtrer les requêtes de contenu statique avec la commande type= </p> </td> 
  </tr> 
 </tbody> 
</table>

## Filtrage du contenu statique {#section-896c37cf68bc446eb0766fb378898262}

Ce mécanisme peut aider à s&#39;assurer que les clients ne reçoivent que des contenus adaptés à leurs besoins. En supposant que le contenu statique soit balisé avec les valeurs `catalog::UserType`appropriées, le client peut ajouter la commande `type=` à la requête. Image Serving compare la valeur fournie avec la commande `type=` à la valeur `catalog::UserType` et, en cas de non-correspondance, renvoie une erreur au lieu de contenu potentiellement inapproprié.

## Voir aussi {#section-91c7b686aacf4d3ca974f35a3fe3d6ec}

[type=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-type.md#reference-89094fd1c50c444eb082cd266769cccb) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Référence du catalogue  [d’images](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
