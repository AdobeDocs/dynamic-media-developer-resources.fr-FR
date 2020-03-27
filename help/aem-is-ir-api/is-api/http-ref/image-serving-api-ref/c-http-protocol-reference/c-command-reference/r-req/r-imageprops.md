---
description: Propriétés de l’image source. Renvoie les propriétés sélectionnées du fichier image ou de l’entrée de catalogue spécifiée dans le chemin d’accès à l’URL.
seo-description: Propriétés de l’image source. Renvoie les propriétés sélectionnées du fichier image ou de l’entrée de catalogue spécifiée dans le chemin d’accès à l’URL.
seo-title: imageprops
solution: Experience Manager
title: imageprops
topic: Scene7 Image Serving - Image Rendering API
uuid: e9bf2780-a520-4fb1-ab4c-40bb799e36a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# imageprops{#imageprops}

Propriétés de l’image source. Renvoie les propriétés sélectionnées du fichier image ou de l’entrée de catalogue spécifiée dans le chemin d’accès à l’URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identifiant de requête unique. </p></td> 
 </tr> 
</table>

La réponse HTTP peut être placée en mémoire cache via le TTL basé sur `attribute::NonImgExpiration`.

Les autres commandes de la chaîne de requête sont ignorées.

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. Default is `s7jsonResponse`.

Les propriétés suivantes sont renvoyées :

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> Propriété</b> </td> 
   <td> <b> Type</b> </td> 
   <td> <b> Description</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catalogue ::Ancre</span> ou point d’ancrage par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalogue ::Expiration</span> ou heure de diffusion par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p>Hauteur d’image en pleine résolution en pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Nom/description du  de associé à cette image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. beddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si le  associé est incorporé dans l’image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.bedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si l’image inclut des données de chemin Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. beddedXmpData</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si l’image inclut des données XMP </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 pour aucun masque, 1 pour alpha prémultiplié, 2 pour alpha non prémultiplié et 3 pour une image de masque distincte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> <span class="codeph"> catalog::Modificateur</span> ou vide, si ce n’est une entrée de catalogue </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. photoshopPathNames</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> des noms de tous les chemins Photoshop associés à cette image, séparé par des virgules </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Le type d’image peut être CMJN, RVB ou BW (pour les images en niveaux de gris). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModificateur</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModificateur</span> ou vide si ce n’est une entrée de catalogue </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> résolution d’impression par défaut en pixels/pouce </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> <span class="codeph"> catalogue::Résolution</span> ou résolution d’objet par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p>Date/heure de modification (à partir du <span class="codeph"> catalogue::TimeStamp</span> ou du fichier image) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbRes</span> ou la résolution de miniature par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalog::ThumbType</span> ou le type de miniature par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Largeur d’image en pleine résolution en pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translateId</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> ID de catalogue auquel l’objet <span class="varname"> spécifié dans le chemin d’accès est résolu (voir</span> Traduction <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"></a>de l’ID d’objet). </p> </td> 
  </tr> 
 </tbody> 
</table>

