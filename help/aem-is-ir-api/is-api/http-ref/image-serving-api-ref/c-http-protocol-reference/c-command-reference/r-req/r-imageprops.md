---
description: Propriétés de l’image source. Renvoie les propriétés sélectionnées du fichier image ou de l’entrée de catalogue spécifiées dans le chemin de l’URL.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 4%

---

# imageprops{#imageprops}

Propriétés de l’image source. Renvoie les propriétés sélectionnées du fichier image ou de l’entrée de catalogue spécifiées dans le chemin de l’URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identifiant unique de la demande. </p></td> 
 </tr> 
</table>

La réponse HTTP peut être mise en cache avec la durée de vie basée sur la base de `attribute::NonImgExpiration`.

Les autres commandes de la chaîne de requête sont ignorées.

Les demandes qui prennent en charge le format de réponse JSONP vous permettent de spécifier le nom du gestionnaire de rappel JS à l’aide de la syntaxe étendue du `req=` paramètre :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` est le nom du gestionnaire JS présent dans la réponse JSONP. Seuls les caractères a-z, A-Z et 0-9 sont autorisés. Optionnel. La valeur par défaut est `s7jsonResponse`.

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
   <td> <p> <span class="codeph"> catalog ::Ancre</span> ou point d’ancrage par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> double </p> </td> 
   <td> <p> <span class="codeph"> catalog ::Expiration</span> ou la durée de vie par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p>Hauteur d’image pleine résolution en pixels </p> </td> 
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
   <td> <p> <span class="codeph"> PhotoshopPaths image.embedded</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si l’image contient Photoshop données de chemin </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. embeddedXmpData</span> </p> </td> 
   <td> <p> boolean </p> </td> 
   <td> <p> 1 si l’image contient des données XMP </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 pour l’absence de masque, 1 pour l’alpha premultiplié, 2 pour l’alpha non prémultiplié et 3 pour une image de masque distincte </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Modificateur d’image.</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> <span class="codeph"> catalog ::Modifier</span> ou vide s’il ne s’agit pas d’une entrée de catalogue </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image. photoshopPathNames</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Liste de noms de tous les chemins d Photoshop associés à cette image séparés par des virgules </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixTyp</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> Type d’image, peut être 'CMJN', 'RVB' ou 'BW' (pour les images en niveaux de gris) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> Modificateur image.postModifier</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> <span class="codeph"> attribut ::P ostModifier</span> ou vide s’il ne s’agit pas d’une entrée de catalogue </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> Résolution d’impression par défaut en pixels/po </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> <span class="codeph"> catalog ::Résolution</span> ou résolution d’objet par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p>Date/heure de modification (à partir de catalog ::TimeStamp<span class="codeph"> ou du </span> fichier image) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> réel </p> </td> 
   <td> <p> <span class="codeph"> catalog ::ThumbRes</span> ou la résolution de miniature par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catalog ::ThumbType</span> ou le type de miniature par défaut </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> entier </p> </td> 
   <td> <p> Largeur d’image pleine résolution en pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.translatedId</span> </p> </td> 
   <td> <p> chaîne </p> </td> 
   <td> <p> ID de catalogue auquel l’objet <span class="varname"></span> spécifié dans le chemin est résolu (voir <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Traduction</a> de l’ID d’objet). </p> </td> 
  </tr> 
 </tbody> 
</table>
