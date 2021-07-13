---
description: Propriétés de l’image source. Renvoie les propriétés sélectionnées du fichier image ou de l’entrée de catalogue spécifiée dans le chemin d’accès à l’URL.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 9%

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

Les requêtes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du paramètre `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Facultatif. La valeur par défaut est `s7jsonResponse`.

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
   <td> <p> <span class="codeph"> catalogue : </span> ancre le point d’ancrage par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalogue : </span> expiration ou heure d’activation par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p>Hauteur d’image en résolution complète en pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Nom/description du profil associé à cette image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. embeddedIccProfile</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si le profil associé est incorporé dans l’image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si l’image inclut des données de chemin Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. embeddedXmpData</span> </p> </td> 
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
   <td> <p> <span class="codeph"> catalogue : </span> Modificateur ou vide s’il ne s’agit pas d’une entrée de catalogue </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. photoshopPathNames</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Liste séparée par des virgules des noms de tous les chemins Photoshop associés à cette image </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Type d’image, peut être "CMJN", "RVB" ou "BW" (pour les images en niveaux de gris) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> <span class="codeph"> attribute::</span> PostModificateurou vide s’il ne s’agit pas d’une entrée de catalogue </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> résolution d’impression par défaut en pixels/pouce </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> <span class="codeph"> catalogue : </span> résolution ou résolution d’objet par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p>Date/heure de modification (à partir du <span class="codeph"> catalogue ::TimeStamp</span> ou du fichier image) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> <span class="codeph"> catalogue : </span> ThumbResor résolution de miniature par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalogue : </span> ThumbTypeor type de miniature par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Largeur d’image en pleine résolution en pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> ID de catalogue auquel l’objet <span class="varname"></span> spécifié dans le chemin d’accès est résolu (voir <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Traduction de l’ID d’objet</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
